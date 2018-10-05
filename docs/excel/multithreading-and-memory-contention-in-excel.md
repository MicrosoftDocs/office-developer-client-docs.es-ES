---
title: Multiproceso y conflictos de memoria en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- subprocesamiento múltiple en excel, funciones de contención de memoria en Excel, funciones [Excel 2007], seguros para subprocesos, subprocesos memoria de proceso local [Excel 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384426"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Multiproceso y conflictos de memoria en Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Las versiones de Microsoft Excel anteriores a Excel 2007 usan un único subproceso para todos los cálculos de la hoja de cálculo. Sin embargo, empezando en Excel 2007, Excel puede configurarse para usar de 1 a 1024 de subprocesos simultáneos para el cálculo de la hoja de cálculo. En un equipo con varios procesadores o varios núcleo, el número predeterminado de subprocesos es igual al número de procesadores o núcleos. Por lo tanto, las celdas de seguros para subprocesos, o las celdas que contienen sólo funciones de seguridad de subprocesos, se pueden asignar a subprocesos simultáneos, sujetos a la lógica de recálculo habitual de que se necesitan se calcula después de sus celdas precedentes.
  
## <a name="thread-safe-functions"></a>Funciones de seguros para subprocesos

La mayoría de las funciones de hoja de cálculo integradas a partir de Excel 2007 es seguros para subprocesos. También puede escribir y registrar funciones XLL como seguros para subprocesos. Excel utiliza un subproceso (su subproceso principal) para llamar a todos los comandos, funciones no seguras subprocesos, funciones **xlAuto** (excepto [xlAutoFree](xlautofree-xlautofree12.md) y **xlAutoFree12**) y COM y Visual Basic para funciones de aplicaciones (VBA).
  
Cuando una función XLL devuelve un **XLOPER** o **XLOPER12** con conjunto de **xlbitDLLFree** , Excel utiliza el mismo subproceso en el que se realizó la llamada de función para llamar a **xlAutoFree** o **xlAutoFree12**. Se realiza la llamada a **xlAutoFree** o **xlAutoFree12** antes de la siguiente llamada de función en el subproceso. 
  
Para los desarrolladores de XLL, existen ventajas para la creación de funciones de subprocesos:
  
- Permiten Excel para sacar el máximo partido en un equipo con varios procesadores o varios núcleo.
    
- Si se abren la posibilidad de usar servidores remotos de forma mucho más eficaz que se puede realizar mediante un único subproceso.
    
Suponga que tiene un equipo de procesador único que se ha configurado para usar, por ejemplo, *N* subprocesos. Suponga que se está ejecutando en una hoja de cálculo que convierte un gran número de llamadas a una función XLL que a su vez envía una solicitud de datos o de un cálculo que se debe realizar en un servidor remoto o un clúster de servidores. Sujeto a la topología del árbol de dependencia, Excel puede llamar a los tiempos de función N casi simultáneamente. Siempre que el servidor o servidores son lo suficientemente rápido o en paralelo, se podría reducir el tiempo de actualización de la hoja de cálculo tanto como un factor de 1/N. 
  
El problema clave en la escritura de las funciones de subprocesos encarga de contención de recursos de correctamente. Normalmente, esto significa contención de memoria y se puede desglosar en dos problemas:
  
- Cómo crear la memoria que sabe que solo se usará este subproceso.
    
- Procedimiento para asegurarse de que la memoria compartida para obtener acceso a varios subprocesos sin ningún riesgo.
    
Lo primero que debe tener en cuenta es qué memoria en un XLL sea accesible para todos los subprocesos, y lo que solo es accesible por el subproceso actualmente en ejecución.
  
 **Puede tener acceso a todos los subprocesos**
  
- Variables, estructuras e instancias de clases se declaran fuera del cuerpo de una función.
    
- Variables estáticas declaradas dentro del cuerpo de una función.
    
En estos dos casos, memoria retirada en el bloque de memoria del archivo DLL creado para esta instancia del archivo DLL. Si otra instancia de la aplicación carga el archivo DLL, obtiene su propia copia de la memoria para que no quede ningún contención para estos recursos desde fuera de la instancia del archivo DLL.
  
 **Sólo puede tener acceso al subproceso actual**
  
- Variables automáticas dentro de código de función (incluidos los argumentos de la función).
    
En este caso, memoria se reserve en la pila para cada instancia de la llamada de función.
  
> [!NOTE]
> El ámbito de memoria asignada dinámicamente depende del ámbito del puntero que señala a ella: si el puntero se encuentra accesible por todos los subprocesos, también es la memoria. Si el puntero es una variable automática en una función, la memoria asignada es privada de forma eficaz a ese subproceso. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Memoria accesible por parte de un único subproceso: memoria Local de subprocesos

Dado que las variables estáticas dentro del cuerpo de una función son accesibles por todos los subprocesos, las funciones que usan claramente no son seguros para subprocesos. Una instancia de la función en un subproceso podría estar cambiando el valor, mientras que otra instancia en otro subproceso asumiendo que sea algo completamente diferente. 
  
Hay dos motivos para declarar variables estáticas dentro de una función:
  
1. Conservan datos estáticos desde una llamada a la siguiente.
    
2. Un puntero a los datos estáticos con seguridad puede ser devuelto por la función.
    
En el caso de primera motivo, es posible que desee tener datos que persiste y tienen significado para todas las llamadas a la función: quizás un contador simple que se incrementa cada vez que se llama a la función en cualquier subproceso, o una estructura que recopila datos de uso y rendimiento en EVA llamada a intentarlo. La pregunta es cómo proteger los datos compartidos o la estructura de datos. Esto se realiza mejor mediante el uso de sección crítica como se explica en la siguiente sección.
  
Si los datos solo está pensados para uso por este subproceso, que podría ser el caso de motivo 1 y siempre es el caso de motivo 2, la pregunta es cómo crear memoria que persiste, pero sólo es accesible desde este subproceso. Una solución consiste en usar el almacenamiento local de subprocesos (TLS) API.
  
Por ejemplo, considere la posibilidad de una función que devuelve un puntero a un **XLOPER**.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Esta función no es segura para subprocesos, debido a que un subproceso puede devolver el estática **XLOPER12** mientras que otro lo sobrescribe. La probabilidad de que esto ocurra es aún mayor si **XLOPER12** necesita que se pasan al **xlAutoFree12**. Una solución consiste en asignar un **XLOPER12**, devolver un puntero a ella e implementar **xlAutoFree12** para que se libera la propia memoria **XLOPER12** . Este método se usa en muchas de las funciones de ejemplo que se muestra en la [Administración de memoria en Excel](memory-management-in-excel.md).
  
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

Este enfoque es más fácil de implementar que el método descrito en la sección siguiente, que se basa en la API de TLS, pero tiene algunas desventajas. En primer lugar, Excel debe llamar **xlAutoFree**/ **xlAutoFree12** con independencia del tipo de devuelto **XLOPER**/ **XLOPER12**. En segundo lugar, hay un problema cuando se devuelva **XLOPER**/ **XLOPER12**s que son el valor devuelto de una llamada a una función de devolución de llamada de la API de C. El **XLOPER**/ **XLOPER12** pueden señalar a la memoria que necesita ser liberados por Excel, pero el **XLOPER**/ se debe liberar**XLOPER12** propio de la misma manera se ha asignado. Si una de esas **XLOPER**/ **XLOPER12** es para usarse como el valor devuelto de una función de hoja de cálculo XLL, no hay ninguna forma sencilla de informar a **xlAutoFree**/ **xlAutoFree12** de la necesidad de liberar ambos punteros de la manera adecuada. (El establecimiento de la **xlbitXLFree** y **xlbitDLLFree** no soluciona el problema, como el tratamiento de **XLOPER/XLOPER12s** en Excel con ambos set no está definido y puede cambiar de una versión a otra.) Para evitar este problema, el XLL puede realizar copias en profundidad de todos los asignados Excel **XLOPER/XLOPER12s** que devuelve a la hoja de cálculo. 
  
Una solución que evita estas limitaciones es rellenar y devolver un subproceso local **XLOPER y XLOPER12**, un método que requiere que **xlAutoFree/xlAutoFree12** que no la libera el puntero **XLOPER y XLOPER12** propio. 
  
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

La siguiente pregunta es cómo configurar y recuperar la memoria local de subprocesos, en otras palabras, cómo implementar la función **get_thread_local_xloper12** en el ejemplo anterior. Esto se realiza mediante el subproceso almacenamiento Local (TLS) API. El primer paso es obtener un índice TLS mediante **TlsAlloc**, que finalmente se deben liberar mediante **TlsFree**. Ambos se realizan mejor desde **DllMain**.
  
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

Después de obtener el índice, el siguiente paso es asignar un bloque de memoria para cada subproceso. La [Documentación de desarrollo de Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) se recomienda hacer esto cada vez que se llama a la función de devolución de llamada de **DllMain** con un evento **DLL_THREAD_ATTACH** y liberar la memoria en cada **DLL_THREAD_DETACH**. Sin embargo, siga este Consejo hará que el archivo DLL realizar el trabajo innecesario para subprocesos que no se usan para el recálculo. 
  
En su lugar, es mejor usar una estrategia de asignación en primer uso. En primer lugar, debe definir una estructura que se va a asignar a cada proceso. Para los ejemplos anteriores que devuelven **XLOPER** o **XLOPER12s**, será suficiente, pero puede crear cualquier estructura que satisfaga sus necesidades.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

La siguiente función obtiene un puntero a la instancia local de subprocesos, o asigna uno si se trata de la primera llamada.
  
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

Ahora puede ver cómo se obtiene la memoria **XLOPER y XLOPER12** local de subproceso: en primer lugar, obtenga un puntero a la instancia del subproceso de **TLS_data**y, a continuación, se devuelve un puntero a la **XLOPER y XLOPER12** contenidos dentro de él, como se indica a continuación. 
  
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

Las funciones **mtr_safe_example_1** y **mtr_safe_example_2** pueden estar registradas como funciones de hoja de cálculo seguros para subprocesos cuando se ejecutan Excel. Sin embargo, no puede mezclar los dos enfoques en un XLL. Su XLL sólo puede exportar una implementación de **xlAutoFree** y **xlAutoFree12**, y cada estrategia de memoria requiere un enfoque diferente. Con **mtr_safe_example_1**, se debe liberar el puntero pasado a **xlAutoFree/xlAutoFree12** junto con los datos que señale a. Con **mtr_safe_example_2**, se deben liberar sólo los datos que apunta a.
  
Windows también proporciona una función **GetCurrentThreadId**, que devuelve el identificador único para todo el sistema. del subproceso actual Esto proporciona el programador con otra forma para que el subproceso de código segura, o para hacer que su subproceso de comportamiento específico.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Memoria accesible sólo mediante más de un subproceso: secciones críticas

Debe proteger la memoria de lectura y escritura que puede tener acceso a más de un subproceso mediante secciones críticas. Necesita una sección crítica con nombre para cada bloque de memoria que desea proteger. Puede inicializar durante la llamada a la función **xlAutoOpen** y liberarlos y establezca en null durante la llamada a la función **xlAutoClose** . A continuación, debe contener cada acceso al bloque protegido dentro de un par de llamadas a **EnterCriticalSection** y **LeaveCriticalSection**. Sólo un subproceso está permitido en la sección crítica en cualquier momento. Este es un ejemplo de la inicialización, desinicialización y uso de una sección denominada **g_csSharedTable**.
  
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

Tal vez más seguro, otra forma de proteger un bloque de memoria es crear una clase que contiene su propia **CRITICAL_SECTION** y cuyo constructor, destructor y los métodos de descriptor de acceso se encargan de su uso. Este enfoque tiene la ventaja de protección de objetos que se pueden inicializar antes de **xlAutoOpen** se ejecuta o sobrevivir después de llamar a **xlAutoClose** , pero debe tener cuidado acerca de la creación de un número excesivo de las secciones críticas y el sistema operativo sobrecarga de la que esto crearía. 
  
Cuando haya código que necesita tener acceso a más de un bloque de memoria protegida al mismo tiempo, debe tener en cuenta el orden en que las secciones críticas entran y salen de cuidadosamente. Por ejemplo, las dos funciones siguientes podrían crear un interbloqueo.
  
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

Si la primera función en un subproceso entra en el **g_csSharedTableA** mientras entra en el segundo en otro subproceso **g_csSharedTableB**, ambos procesos se bloquean. El enfoque correcto es escribe en un orden coherente y la salida en el orden inverso, como se indica a continuación.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Siempre que sea posible, es mejor desde un subproceso cooperación punto de vista para aislar el acceso a distintos bloques, como se muestra aquí.
  
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

Donde hay una gran cantidad de contención para un recurso compartido, como las solicitudes de acceso frecuente de corta duración, considere la posibilidad de uso de capacidad de la sección crítica para girar. Ésta es una técnica que pone en espera para el recurso menos intensivos del procesador. Para ello, puede utilizar cualquiera **InitializeCriticalSectionAndSpinCount** al inicializar la sección o **SetCriticalSectionSpinCount** una vez inicializada, para establecer el número de veces que el subproceso realiza un bucle antes de esperar para convertirse en los recursos de se encuentra disponible. La operación de espera es cara, por lo que girando Esto evita si el recurso se libera muchísimo. En un sistema de procesador único, el número de recombinaciones de forma eficaz se pasa por alto, pero aún se puede especificar sin problemas. El administrador del montón de memoria usa un recuento de rotación de 4000. Para obtener más información acerca del uso de secciones críticas, consulte la documentación del SDK de Windows. 
  
## <a name="see-also"></a>Vea también



[Administración de memoria en Excel](memory-management-in-excel.md)
  
[Actualización multiproceso en Excel](multithreaded-recalculation-in-excel.md)
  
[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)

