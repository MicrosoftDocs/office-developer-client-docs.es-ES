---
title: Multiproceso y conTención de memoria en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- multiproceso en Excel, contención de memoria en Excel, funciones [Excel 2007], funciones seguras para subprocesos, seguridad para subprocesos [Excel 2007], memoria local de subproceso [Excel 2007]
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
# <a name="multithreading-and-memory-contention-in-excel"></a>Multiproceso y conTención de memoria en Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Las versiones de Microsoft Excel anteriores a Excel 2007 usar un único subproceso para todos los cálculos de la hoja de cálculo. Sin embargo, a partir de Excel 2007, Excel se puede configurar para usar de 1 a 1024 subprocesos simultáneos para el cálculo de la hoja de cálculo. En un equipo con varios procesadores o varios núcleos, el número predeterminado de subprocesos es igual al número de procesadores o núcleos. Por lo tanto, las celdas seguras para subprocesos o las celdas que solo contienen funciones que son seguras para subprocesos, se pueden asignar a subprocesos simultáneos, sujeto a la lógica de recálculo habitual que necesita calcularse después de sus precedentes.
  
## <a name="thread-safe-functions"></a>Funciones seguras para subProcesos

La mayoría de las funciones integradas de hoja de cálculo que se inician en Excel 2007 son seguras para subprocesos. También puede escribir y registrar funciones XLL como seguras para subprocesos. Excel utiliza un subproceso (su subproceso principal) para llamar a todos los comandos, funciones no seguras de subprocesos, funciones **xlAuto** (excepto [xlAutoFree](xlautofree-xlautofree12.md) y **XLAUTOFREE12**) y funciones de com y Visual Basic para aplicaciones (VBA).
  
Cuando una función XLL devuelve **XLOPER** o **XLOPER12** con **xlbitDLLFree** establecido, Excel usa el mismo subproceso en el que se realizó la llamada de función para llamar a **xlAutoFree** o **xlAutoFree12**. La llamada a **xlAutoFree** o **xlAutoFree12** se realiza antes de la siguiente llamada de función en ese subproceso. 
  
Para los desarrolladores de XLL, hay ventajas para crear funciones seguras para subprocesos:
  
- Permiten a Excel aprovechar al máximo un equipo de varios núcleos o varios procesadores.
    
- Abrirán la posibilidad de usar servidores remotos de forma mucho más eficaz de lo que se puede hacer con un único subproceso.
    
Suponga que tiene un equipo de un solo procesador que se ha configurado para usar, por ejemplo, *N* subprocesos. SuPongamos que se está ejecutando una hoja de cálculo que realiza un gran número de llamadas a una función XLL que, a su vez, envía una solicitud de datos o que se va a realizar un cálculo en un servidor remoto o un clúster de servidores. Sujeto a la topología del árbol de dependencias, Excel podría llamar a la función N veces de forma casi simultánea. Siempre que el servidor o los servidores sean lo suficientemente rápidos o paralelos, el tiempo de recálculo de la hoja de cálculo podría reducirse hasta un factor de 1/N. 
  
El problema clave al escribir funciones seguras para subprocesos es controlar la contención de los recursos correctamente. Esto suele significar una contención de la memoria y puede dividirse en dos aspectos:
  
- Cómo crear memoria que solo sabrá que usará este subproceso.
    
- Cómo garantizar que varios subprocesos obtengan acceso a la memoria compartida de forma segura.
    
Lo primero que debe tener en cuenta es qué memoria de un XLL es accesible para todos los subprocesos y a qué solo tiene acceso el subproceso que se está ejecutando actualmente.
  
 **Accesible para todos los subprocesos**
  
- Variables, estructuras e instancias de clase declaradas fuera del cuerpo de una función.
    
- Variables estáticas declaradas en el cuerpo de una función.
    
En estos dos casos, la memoria se reserva en el bloque de memoria del DLL creado para esta instancia del archivo DLL. Si otra instancia de la aplicación carga la DLL, obtiene su propia copia de esa memoria para que no haya contención para estos recursos desde fuera de esta instancia del DLL.
  
 **Accesible solo por el subproceso actual**
  
- Variables automáticas en el código de función (incluidos argumentos de función).
    
En este caso, la memoria se reserva en la pila para cada instancia de la llamada de función.
  
> [!NOTE]
> El ámbito de la memoria asignada dinámicamente depende del ámbito del puntero que apunta a ella: si todos los subprocesos pueden obtener acceso al puntero, la memoria también es. Si el puntero es una variable automática en una función, la memoria asignada es realmente privada para ese hilo. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Memoria accesible solo para un subProceso: memoria de subProceso local

Dado que las variables estáticas dentro del cuerpo de una función son accesibles por todos los subprocesos, las funciones que las usan no son claramente seguras para subprocesos. Una instancia de la función en un subproceso podría cambiar el valor mientras que otra instancia en otro subproceso asume que es un proceso completamente diferente. 
  
Hay dos razones para declarar variables estáticas dentro de una función:
  
1. Los datos estáticos se conservan de una llamada a la siguiente.
    
2. La función puede devolver de forma segura un puntero a datos estáticos.
    
En el caso del primer motivo, es posible que desee tener datos que persisten y tienen significado para todas las llamadas a la función: por ejemplo, un contador sencillo que se incrementa cada vez que se llama a la función en cualquier subproceso o una estructura que recopila datos de rendimiento y uso en Eva llamada Ry. La pregunta es cómo proteger los datos compartidos o la estructura de datos. Para ello, se recomienda usar la sección crítica como se explica en la sección siguiente.
  
Si los datos están destinados para su uso con este subproceso, que podrían ser el caso de la razón 1 y siempre es el caso del motivo 2, la pregunta es cómo crear memoria que persisten pero que solo es accesible desde este subproceso. Una solución es usar la API de almacenamiento local de subprocesos (TLS).
  
Por ejemplo, considere una función que devuelve un puntero a un **XLOPER**.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Esta función no es segura para subprocesos porque un subproceso puede devolver el valor estático de **XLOPER12** mientras que otra la sobrescribe. La probabilidad de que esto suceda es mayor aún si **XLOPER12** necesita pasarse a **xlAutoFree12**. Una solución es asignar un **XLOPER12**, devolver un puntero a él e implementar **xlAutoFree12** para liberar la memoria de **xloper12** . Este método se usa en muchas de las funciones de ejemplo que se muestran en la [Administración de memoria en Excel](memory-management-in-excel.md).
  
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

Este enfoque es más fácil de implementar que el planteamiento descrito en la siguiente sección, que se basa en la API de TLS, pero tiene algunas desventajas. En primer lugar, Excel debe llamar a **xlAutoFree**/ **xlAutoFree12** cualquiera que sea el tipo de**XLOPER12**de **XLOPER**/ devuelto. En segundo lugar, se produce un problema al devolver **XLOPER**/ o**XLOPER12**s que son el valor devuelto de una llamada a una función de devolución de llamada de la API de C. El ****/ **xloper12** de XLOPER puede apuntar a memoria que debe ser liberada por Excel, pero el propio**xloper12** de **XLOPER**/ debe liberarse de la misma manera en que se asignó. Si se va a usar un tipo**XLOPER12** de **XLOPER**/ como valor devuelto de una función XLL de hoja de cálculo, no hay una forma sencilla de informar a **xlAutoFree**/ **xlAutoFree12** de la necesidad de liberar ambos punteros de la forma adecuada. (Al establecer tanto **xlbitXLFree** como **xlbitDLLFree** no se soluciona el problema, ya que el tratamiento de **XLOPER/xloper12** en Excel con ambos set no está definido y puede cambiar de una versión a la versión). Para solucionar este problema, el XLL puede hacer copias en profundidad de los **XLOPER y xloper12** asignados a Excel que vuelve a la hoja de cálculo. 
  
Una solución que evita estas limitaciones es rellenar y devolver un **XLOPER o xloper12**de subproceso local, un enfoque que necesita que **xlAutoFree/xlAutoFree12** no libere el puntero **XLOPER o xloper12** en sí. 
  
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

La siguiente pregunta es cómo configurar y recuperar la memoria local de subprocesos, es decir, cómo implementar la función **get_thread_local_xloper12** en el ejemplo anterior. Esto se realiza mediante la API de almacenamiento local de subProcesos (TLS). El primer paso consiste en obtener un índice TLS mediante **TlsAlloc**, que debe estar disponible en última instancia con **TlsFree**. Las dos se realizan mejor desde **DllMain**.
  
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

Después de obtener el índice, el siguiente paso consiste en asignar un bloque de memoria para cada subproceso. La [documentación de desarrollo de Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recomienda hacer esto cada vez que se llama a la función de devolución de llamada **DllMain** con un evento **DLL_THREAD_ATTACH** y liberar la memoria en cada **DLL_THREAD_DETACH**. Sin embargo, si sigue este Consejo, el DLL hará un trabajo innecesario para subprocesos que no se usan para la actualización. 
  
En su lugar, es mejor usar una estrategia de asignación de primer uso. En primer lugar, debe definir una estructura que desee asignar para cada subproceso. Para los ejemplos anteriores que devuelven **XLOPER** o **xloper12**, basta con lo siguiente, pero puede crear cualquier estructura que satisfaga sus necesidades.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

La siguiente función obtiene un puntero a la instancia de subproceso local o asigna una si esta es la primera llamada.
  
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

Ahora puede ver cómo se obtiene la memoria de **XLOPER o XLOPER12** de subproceso local: en primer lugar, se obtiene un puntero a la instancia del subproceso **TLS_data**y, a continuación, se devuelve un puntero a **XLOPER o XLOPER12** que se incluye en él, como se indica a continuación. 
  
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

Las funciones **mtr_safe_example_1** y **mtr_safe_example_2** pueden registrarse como funciones de hoja de cálculo seguras para subprocesos cuando se ejecuta Excel. Sin embargo, no se pueden mezclar los dos enfoques en un XLL. El XLL solo puede exportar una implementación de **xlAutoFree** y **xlAutoFree12**, y cada estrategia de memoria requiere un enfoque diferente. Con **mtr_safe_example_1**, el puntero que se pasa a **xlAutoFree/xlAutoFree12** debe liberarse junto con los datos a los que apunta. Con **mtr_safe_example_2**, solo deben liberarse los datos señalados.
  
Windows también proporciona una función **GetCurrentThreadId**, que devuelve el identificador único de todo el sistema del subproceso actual. Esto proporciona al desarrollador otra forma de hacer que el subproceso de código sea seguro o hacer que su comportamiento sea específico.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Memoria accesible solo por más de un subProceso: secciones críticas

Debe proteger la memoria de lectura y escritura a la que se puede tener acceso a través de más de un subproceso con secciones críticas. Necesita una sección crítica con nombre para cada bloque de memoria que quiera proteger. Puede inicializarlos durante la llamada a la función **xlAutoOpen** , liberarlos y establecerlos en NULL durante la llamada a la función **xlAutoClose** . A continuación, debe incluir cada acceso al bloque protegido dentro de un par de llamadas a **EnterCriticalSection** y **LeaveCriticalSection**. Solo se permite un subproceso en la sección crítica en cualquier momento. A continuación, se muestra un ejemplo de la inicialización, la desinicialización y el uso de una sección denominada **g_csSharedTable**.
  
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

Otro modo más seguro de proteger un bloque de memoria es crear una clase que contenga su propio **critical_section** y cuyo constructor, destructor y métodos de descriptor de acceso se ocupen de su uso. Este enfoque tiene la ventaja adicional de proteger objetos que se pueden inicializar antes de que se ejecute **xlAutoOpen** o sobrevivir después de llamar a **xlAutoClose** , pero debe tener cuidado con la creación de muchas secciones críticas y el sistema operativo. sobrecarga que crearía. 
  
Cuando tiene código que necesita tener acceso a más de un bloque de memoria protegida al mismo tiempo, debe tener en cuenta con cuidado el orden en el que se entran y salen las secciones críticas. Por ejemplo, las dos funciones siguientes podrían crear un interbloqueo.
  
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

Si la primera función de un subproceso introduce **g_csSharedTableA** mientras que la segunda de otro subproceso escribe **g_csSharedTableB**, ambos subprocesos se bloquean. El método correcto es escribir en un orden coherente y salir en orden inverso, como se indica a continuación.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Siempre que sea posible, es mejor hacerlo desde el punto de vista de cooperabilidad de un subproceso para aislar el acceso a distintos bloques, tal como se muestra aquí.
  
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

Cuando hay una gran cantidad de contención para un recurso compartido, como las solicitudes de acceso frecuentes de corta duración, debe considerar el uso de la capacidad de la sección crítica para girar. Se trata de una técnica que hace que la espera del recurso consuma menos uso del procesador. Para ello, puede usar cualquiera de las **InitializeCriticalSectionAndSpinCount** al inicializar la sección o **SetCriticalSectionSpinCount** una vez inicializada, para establecer el número de veces que se recorre el subproceso antes de esperar a que los recursos se conviertan en disponga. La operación de espera es costosa, por lo que el giro evita que se libere el recurso mientras tanto. En un sistema de un solo procesador, el recuento de giros se omite de manera efectiva, pero puede especificarlo sin que se dañe. El administrador del montón de memoria usa un recuento circular de 4000. Para obtener más información acerca del uso de las secciones críticas, consulte la documentación del SDK de Windows. 
  
## <a name="see-also"></a>Vea también



[Administración de memoria en Excel](memory-management-in-excel.md)
  
[Actualización multiproceso en Excel](multithreaded-recalculation-in-excel.md)
  
[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)

