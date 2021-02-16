---
title: Multithreading y contención de memoria en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- multithreading en excel,contención de memoria en Excel,functions [Excel 2007], thread-safe,thread-safe functions [Excel 2007],thread-local memory [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301641"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Multithreading y contención de memoria en Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Las versiones de Microsoft Excel anteriores a Excel 2007 usan un único subproceso para todos los cálculos de hoja de cálculo. Sin embargo, a partir de Excel 2007, Excel se puede configurar para usar de 1 a 1024 subprocesos simultáneos para el cálculo de la hoja de cálculo. En un equipo con varios procesadores o varios núcleos, el número predeterminado de subprocesos es igual al número de procesadores o núcleos. Por lo tanto, las celdas seguras para subprocesos, o las celdas que solo contienen funciones seguras para subprocesos, pueden asignase a subprocesos simultáneos, sujeto a la lógica de recálculo habitual de la necesidad de calcularse después de sus precedentes.
  
## <a name="thread-safe-functions"></a>Thread-Safe funciones

La mayoría de las funciones de hoja de cálculo integradas a partir de Excel 2007 son seguras para subprocesos. También puedes escribir y registrar funciones XLL como seguras para subprocesos. Excel usa un subproceso (su subproceso principal) para llamar a todos los comandos, funciones no seguras para subprocesos, funciones **xlAuto** (excepto [xlAutoFree](xlautofree-xlautofree12.md) y **xlAutoFree12)** y funciones COM y Visual Basic para Aplicaciones (VBA).
  
Cuando una función XLL devuelve un **XLOPER** o **XLOPER12** con **xlbitDLLFree** establecido, Excel usa el mismo subproceso en el que se realizó la llamada de función para llamar a **xlAutoFree** o **xlAutoFree12**. La llamada a **xlAutoFree** o **xlAutoFree12** se realiza antes de la siguiente llamada de función en ese subproceso. 
  
Para los desarrolladores de XLL, hay ventajas para crear funciones seguras para subprocesos:
  
- Permiten a Excel obtener el máximo partido de un equipo multiprocesador o de varios núcleos.
    
- Abren la posibilidad de usar servidores remotos de forma mucho más eficaz de lo que se puede hacer con un solo subproceso.
    
Supongamos que tiene un equipo con un solo procesador que se ha configurado para usar, por ejemplo,  *N*  subprocesos. Suponga que se está ejecutando una hoja de cálculo que realiza un gran número de llamadas a una función XLL que, a su vez, envía una solicitud de datos o para que se realice un cálculo a un servidor remoto o clúster de servidores. Sujeto a la topología del árbol de dependencias, Excel podría llamar a la función N veces casi simultáneamente. Siempre que el servidor o los servidores sean lo suficientemente rápidos o paralelos, el tiempo de actualización de la hoja de cálculo podría reducirse hasta un factor de 1/N. 
  
El problema clave en la escritura de funciones seguras para subprocesos es controlar la contención de recursos correctamente. Esto suele significar contención de memoria y se puede dividir en dos problemas:
  
- Este subproceso solo usará la memoria que sabe.
    
- Cómo garantizar que varios subprocesos acceden a la memoria compartida de forma segura.
    
Lo primero que debe tener en cuenta es qué memoria de un XLL es accesible para todos los subprocesos y qué solo puede tener acceso el subproceso que se está ejecutando actualmente.
  
 **Accesible para todos los subprocesos**
  
- Variables, estructuras e instancias de clase declaradas fuera del cuerpo de una función.
    
- Variables estáticas declaradas en el cuerpo de una función.
    
En estos dos casos, la memoria se reserva en el bloque de memoria del DLL creado para esta instancia de la DLL. Si otra instancia de aplicación carga la DLL, obtiene su propia copia de esa memoria para que no haya contención para estos recursos desde fuera de esta instancia de la DLL.
  
 **Accesible solo por el subproceso actual**
  
- Variables automáticas dentro del código de función (incluidos los argumentos de función).
    
En este caso, la memoria se reserva en la pila para cada instancia de la llamada de función.
  
> [!NOTE]
> El ámbito de la memoria asignada dinámicamente depende del ámbito del puntero que apunta a él: si todos los subprocesos tienen acceso al puntero, la memoria también lo es. Si el puntero es una variable automática en una función, la memoria asignada es efectivamente privada para ese subproceso. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Memoria accesible solo por un subproceso: Thread-Local memoria

Dado que todos los subprocesos pueden tener acceso a las variables estáticas dentro del cuerpo de una función, las funciones que las usan claramente no son seguras para subprocesos. Una instancia de la función en un subproceso podría estar cambiando el valor mientras que otra instancia en otro subproceso asume que es algo completamente diferente. 
  
Hay dos razones para declarar variables estáticas dentro de una función:
  
1. Los datos estáticos persisten de una llamada a la siguiente.
    
2. La función puede devolver de forma segura un puntero a datos estáticos.
    
En el caso de la primera razón, es posible que desee tener datos que persistan y tengan significado para todas las llamadas a la función: quizás un contador simple que se incrementa cada vez que se llama a la función en cualquier subproceso, o una estructura que recopila datos de uso y rendimiento en cada llamada. La pregunta es cómo proteger la estructura de datos o datos compartidos. Esto se realiza mejor mediante el uso de la sección crítica como se explica en la siguiente sección.
  
Si los datos están pensados solo para su uso por este subproceso, que podría ser el caso de la razón 1 y siempre es el caso de la razón 2, la pregunta es cómo crear memoria que persiste pero solo es accesible desde este subproceso. Una solución es usar la API de almacenamiento local de subprocesos (TLS).
  
Por ejemplo, considere una función que devuelve un puntero a **un XLOPER**.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Esta función no es segura para subprocesos porque un subproceso puede devolver el **XLOPER12** estático mientras que otro la sobrescribe. La probabilidad de que esto suceda es mayor aún si **el XLOPER12** debe pasarse a **xlAutoFree12**. Una solución es asignar un **XLOPER12,** devolver un puntero a él e implementar **xlAutoFree12** para que se libera la memoria **XLOPER12** en sí. Este enfoque se usa en muchas de las funciones de ejemplo que se muestran en [Administración de memoria en Excel](memory-management-in-excel.md).
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

Este enfoque es más sencillo de implementar que el que se describe en la siguiente sección, que se basa en la API de TLS, pero tiene algunas desventajas. En primer lugar, Excel debe llamar **a xlAutoFree** xlAutoFree12 independientemente del tipo de /   **XLOPER** /  **XLOPER12 devuelto.** En segundo lugar, hay un problema al devolver **XLOPER** /  **XLOPER12** que son el valor devuelto de una llamada a una función de devolución de llamada de la API de C. **XLOPER** XLOPER12 puede apuntar a la memoria que Excel necesita liberar, pero el propio /    /  **XLOPER XLOPER12** debe liberarse de la misma manera que se asignó. Si se va a usar un /  **XLOPER XLOPER12** como valor devuelto de una función de hoja de cálculo XLL, no hay una forma fácil de informar a **xlAutoFree** /  **xlAutoFree12** de la necesidad de liberar ambos punteros de la manera adecuada. (Establecer **xlbitXLFree** y **xlbitDLLFree** no resuelve el problema, ya que el tratamiento de **XLOPER/XLOPER12 en** Excel con ambos establecidos no está definido y puede cambiar de una versión a otra). Para solucionar este problema, el XLL puede hacer copias en profundidad de todos los **XLOPER/XLOPER12 asignados** por Excel que devuelve a la hoja de cálculo. 
  
Una solución que evite estas limitaciones es rellenar y devolver un **XLOPER/XLOPER12** local para subprocesos, un enfoque que necesita que **xlAutoFree/xlAutoFree12** no libera el propio puntero **XLOPER/XLOPER12.** 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

La siguiente pregunta es cómo configurar y recuperar la memoria local del subproceso, es decir, cómo implementar la función **get_thread_local_xloper12** en el ejemplo anterior. Esto se realiza mediante la API de almacenamiento local de subprocesos (TLS). El primer paso es obtener un índice TLS mediante **TlsAlloc**, que en última instancia debe liberarse con **TlsFree**. Ambos se logran mejor desde **DllMain**.
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

Después de obtener el índice, el siguiente paso es asignar un bloque de memoria para cada subproceso. La [documentación de desarrollo](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) de Windows recomienda hacer esto cada vez que se llama a la función de devolución de llamada **DllMain** con un evento **DLL_THREAD_ATTACH** y liberar la memoria en cada DLL_THREAD_DETACH **.** Sin embargo, seguir este consejo haría que la DLL realizara un trabajo innecesario para subprocesos que no se usan para la actualización. 
  
En su lugar, es mejor usar una estrategia de asignación de uso por primera vez. En primer lugar, debes definir una estructura que quieras asignar para cada subproceso. Para los ejemplos anteriores que devuelven **XLOPER12 o XLOPER12,** basta con lo siguiente, pero puede crear cualquier estructura que satisfaga sus necesidades. 
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

La siguiente función obtiene un puntero a la instancia local del subproceso o asigna uno si esta es la primera llamada.
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

Ahora puede ver cómo se obtiene la memoria **XLOPER/XLOPER12** local del subproceso: primero, obtiene un puntero a la instancia del subproceso de TLS_data y, **a** continuación, devuelve un puntero al **XLOPER/XLOPER12** que contiene, como se muestra a continuación. 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

Las **mtr_safe_example_1** y **mtr_safe_example_2** pueden registrarse como funciones de hoja de cálculo seguras para subprocesos cuando se ejecuta Excel. Sin embargo, no puede mezclar los dos enfoques en un XLL. El XLL solo puede exportar una implementación de **xlAutoFree** y **xlAutoFree12,** y cada estrategia de memoria requiere un enfoque diferente. Con **mtr_safe_example_1,** el puntero pasado a **xlAutoFree/xlAutoFree12** debe liberarse junto con los datos a los que señala. Con **mtr_safe_example_2,** solo se liberarán los datos señalados.
  
Windows también proporciona una función **GetCurrentThreadId**, que devuelve el identificador único de todo el sistema del subproceso actual. Esto proporciona al desarrollador otra forma de hacer que el subproceso de código sea seguro o de hacer que su subproceso de comportamiento sea específico.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Memoria accesible solo por más de un subproceso: secciones críticas

Debes proteger la memoria de lectura y escritura a la que pueda acceder más de un subproceso mediante secciones críticas. Necesita una sección crítica con nombre para cada bloque de memoria que desee proteger. Puede inicializarlos durante la llamada a la función **xlAutoOpen,** liberarlos y establecerlos en null durante la llamada a la **función xlAutoClose.** A continuación, debe contener cada acceso al bloque protegido dentro de un par de llamadas a **EnterCriticalSection** y **LeaveCriticalSection**. Solo se permite un subproceso en la sección crítica en cualquier momento. Este es un ejemplo de inicialización, deserialización y uso de una sección denominada **g_csSharedTable**.
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

Otra forma, quizás más segura de proteger un bloque de memoria, es crear una clase que contenga su propio **CRITICAL_SECTION** y cuyo constructor, destructor y métodos de acceso se encargan de su uso. Este enfoque tiene la ventaja adicional de proteger objetos que se pueden inicializar antes de que se ejecute **xlAutoOpen** o sobrevivíen después de llamar a **xlAutoClose,** pero debes tener cuidado al crear demasiadas secciones críticas y la sobrecarga del sistema operativo que esto crearía. 
  
Cuando tenga código que necesite tener acceso a más de un bloque de memoria protegida al mismo tiempo, debe tener muy en cuenta el orden en que se introducen y salen las secciones críticas. Por ejemplo, las dos funciones siguientes podrían crear un interbloqueo.
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Si la primera función de un subproceso entra en **g_csSharedTableA** mientras que la segunda en otro subproceso entra en **g_csSharedTableB**, ambos subprocesos se cuelgan. El enfoque correcto es escribir en un orden coherente y salir en el orden inverso, como se muestra a continuación.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Siempre que sea posible, es mejor desde un punto de vista de co-operación de subprocesos aislar el acceso a bloques distintos, como se muestra aquí.
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Cuando haya mucha contención para un recurso compartido, como las solicitudes de acceso de corta duración frecuentes, debe considerar la posibilidad de usar la capacidad de girar de la sección crítica. Se trata de una técnica que hace que la espera para el recurso sea menos intensiva en el procesador. Para ello, puedes usar **InitializeCriticalSectionAndSpinCount** al inicializar la sección o **SetCriticalSectionSpinCount** una vez inicializado, para establecer el número de veces que el subproceso se bucle antes de esperar a que los recursos estén disponibles. La operación de espera es costosa, por lo que girar evita esto si el recurso se libera mientras tanto. En un sistema de procesador único, el número de giros se omite de forma eficaz, pero aún puedes especificarlo sin causar ningún daño. El administrador de montón de memoria usa un recuento de número de 4000. Para obtener más información sobre el uso de secciones críticas, consulta la documentación de Windows SDK. 
  
## <a name="see-also"></a>Consulte también



[Administración de memoria en Excel](memory-management-in-excel.md)
  
[Actualización multiproceso en Excel](multithreaded-recalculation-in-excel.md)
  
[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)

