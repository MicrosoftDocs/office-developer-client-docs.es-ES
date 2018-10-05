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
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="c3bc9-104">Multiproceso y conflictos de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="c3bc9-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="c3bc9-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c3bc9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c3bc9-106">Las versiones de Microsoft Excel anteriores a Excel 2007 usan un único subproceso para todos los cálculos de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="c3bc9-107">Sin embargo, empezando en Excel 2007, Excel puede configurarse para usar de 1 a 1024 de subprocesos simultáneos para el cálculo de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="c3bc9-108">En un equipo con varios procesadores o varios núcleo, el número predeterminado de subprocesos es igual al número de procesadores o núcleos.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="c3bc9-109">Por lo tanto, las celdas de seguros para subprocesos, o las celdas que contienen sólo funciones de seguridad de subprocesos, se pueden asignar a subprocesos simultáneos, sujetos a la lógica de recálculo habitual de que se necesitan se calcula después de sus celdas precedentes.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="c3bc9-110">Funciones de seguros para subprocesos</span><span class="sxs-lookup"><span data-stu-id="c3bc9-110">Thread-Safe Functions</span></span>

<span data-ttu-id="c3bc9-111">La mayoría de las funciones de hoja de cálculo integradas a partir de Excel 2007 es seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-111">Most of the built-in worksheet functions starting in Excel 2007 are thread safe.</span></span> <span data-ttu-id="c3bc9-112">También puede escribir y registrar funciones XLL como seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-112">You can also write and register XLL functions as being thread safe.</span></span> <span data-ttu-id="c3bc9-113">Excel utiliza un subproceso (su subproceso principal) para llamar a todos los comandos, funciones no seguras subprocesos, funciones **xlAuto** (excepto [xlAutoFree](xlautofree-xlautofree12.md) y **xlAutoFree12**) y COM y Visual Basic para funciones de aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="c3bc9-113">Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="c3bc9-114">Cuando una función XLL devuelve un **XLOPER** o **XLOPER12** con conjunto de **xlbitDLLFree** , Excel utiliza el mismo subproceso en el que se realizó la llamada de función para llamar a **xlAutoFree** o **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-114">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**.</span></span> <span data-ttu-id="c3bc9-115">Se realiza la llamada a **xlAutoFree** o **xlAutoFree12** antes de la siguiente llamada de función en el subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-115">The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="c3bc9-116">Para los desarrolladores de XLL, existen ventajas para la creación de funciones de subprocesos:</span><span class="sxs-lookup"><span data-stu-id="c3bc9-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="c3bc9-117">Permiten Excel para sacar el máximo partido en un equipo con varios procesadores o varios núcleo.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="c3bc9-118">Si se abren la posibilidad de usar servidores remotos de forma mucho más eficaz que se puede realizar mediante un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="c3bc9-119">Suponga que tiene un equipo de procesador único que se ha configurado para usar, por ejemplo, *N* subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-119">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads.</span></span> <span data-ttu-id="c3bc9-120">Suponga que se está ejecutando en una hoja de cálculo que convierte un gran número de llamadas a una función XLL que a su vez envía una solicitud de datos o de un cálculo que se debe realizar en un servidor remoto o un clúster de servidores.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-120">Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers.</span></span> <span data-ttu-id="c3bc9-121">Sujeto a la topología del árbol de dependencia, Excel puede llamar a los tiempos de función N casi simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-121">Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously.</span></span> <span data-ttu-id="c3bc9-122">Siempre que el servidor o servidores son lo suficientemente rápido o en paralelo, se podría reducir el tiempo de actualización de la hoja de cálculo tanto como un factor de 1/N.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-122">Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="c3bc9-123">El problema clave en la escritura de las funciones de subprocesos encarga de contención de recursos de correctamente.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-123">The key issue in writing thread-safe functions is handling contention for resources correctly.</span></span> <span data-ttu-id="c3bc9-124">Normalmente, esto significa contención de memoria y se puede desglosar en dos problemas:</span><span class="sxs-lookup"><span data-stu-id="c3bc9-124">This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="c3bc9-125">Cómo crear la memoria que sabe que solo se usará este subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="c3bc9-126">Procedimiento para asegurarse de que la memoria compartida para obtener acceso a varios subprocesos sin ningún riesgo.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="c3bc9-127">Lo primero que debe tener en cuenta es qué memoria en un XLL sea accesible para todos los subprocesos, y lo que solo es accesible por el subproceso actualmente en ejecución.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="c3bc9-128">**Puede tener acceso a todos los subprocesos**</span><span class="sxs-lookup"><span data-stu-id="c3bc9-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="c3bc9-129">Variables, estructuras e instancias de clases se declaran fuera del cuerpo de una función.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="c3bc9-130">Variables estáticas declaradas dentro del cuerpo de una función.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="c3bc9-131">En estos dos casos, memoria retirada en el bloque de memoria del archivo DLL creado para esta instancia del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-131">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL.</span></span> <span data-ttu-id="c3bc9-132">Si otra instancia de la aplicación carga el archivo DLL, obtiene su propia copia de la memoria para que no quede ningún contención para estos recursos desde fuera de la instancia del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-132">If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="c3bc9-133">**Sólo puede tener acceso al subproceso actual**</span><span class="sxs-lookup"><span data-stu-id="c3bc9-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="c3bc9-134">Variables automáticas dentro de código de función (incluidos los argumentos de la función).</span><span class="sxs-lookup"><span data-stu-id="c3bc9-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="c3bc9-135">En este caso, memoria se reserve en la pila para cada instancia de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c3bc9-136">El ámbito de memoria asignada dinámicamente depende del ámbito del puntero que señala a ella: si el puntero se encuentra accesible por todos los subprocesos, también es la memoria.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-136">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also.</span></span> <span data-ttu-id="c3bc9-137">Si el puntero es una variable automática en una función, la memoria asignada es privada de forma eficaz a ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-137">If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="c3bc9-138">Memoria accesible por parte de un único subproceso: memoria Local de subprocesos</span><span class="sxs-lookup"><span data-stu-id="c3bc9-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="c3bc9-139">Dado que las variables estáticas dentro del cuerpo de una función son accesibles por todos los subprocesos, las funciones que usan claramente no son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-139">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe.</span></span> <span data-ttu-id="c3bc9-140">Una instancia de la función en un subproceso podría estar cambiando el valor, mientras que otra instancia en otro subproceso asumiendo que sea algo completamente diferente.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-140">One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="c3bc9-141">Hay dos motivos para declarar variables estáticas dentro de una función:</span><span class="sxs-lookup"><span data-stu-id="c3bc9-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="c3bc9-142">Conservan datos estáticos desde una llamada a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="c3bc9-143">Un puntero a los datos estáticos con seguridad puede ser devuelto por la función.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="c3bc9-144">En el caso de primera motivo, es posible que desee tener datos que persiste y tienen significado para todas las llamadas a la función: quizás un contador simple que se incrementa cada vez que se llama a la función en cualquier subproceso, o una estructura que recopila datos de uso y rendimiento en EVA llamada a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-144">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call.</span></span> <span data-ttu-id="c3bc9-145">La pregunta es cómo proteger los datos compartidos o la estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-145">The question is how to protect the shared data or data structure.</span></span> <span data-ttu-id="c3bc9-146">Esto se realiza mejor mediante el uso de sección crítica como se explica en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-146">This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="c3bc9-147">Si los datos solo está pensados para uso por este subproceso, que podría ser el caso de motivo 1 y siempre es el caso de motivo 2, la pregunta es cómo crear memoria que persiste, pero sólo es accesible desde este subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-147">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread.</span></span> <span data-ttu-id="c3bc9-148">Una solución consiste en usar el almacenamiento local de subprocesos (TLS) API.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-148">One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="c3bc9-149">Por ejemplo, considere la posibilidad de una función que devuelve un puntero a un **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="c3bc9-150">Esta función no es segura para subprocesos, debido a que un subproceso puede devolver el estática **XLOPER12** mientras que otro lo sobrescribe.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-150">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it.</span></span> <span data-ttu-id="c3bc9-151">La probabilidad de que esto ocurra es aún mayor si **XLOPER12** necesita que se pasan al **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-151">The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**.</span></span> <span data-ttu-id="c3bc9-152">Una solución consiste en asignar un **XLOPER12**, devolver un puntero a ella e implementar **xlAutoFree12** para que se libera la propia memoria **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="c3bc9-152">One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed.</span></span> <span data-ttu-id="c3bc9-153">Este método se usa en muchas de las funciones de ejemplo que se muestra en la [Administración de memoria en Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="c3bc9-153">This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
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

<span data-ttu-id="c3bc9-154">Este enfoque es más fácil de implementar que el método descrito en la sección siguiente, que se basa en la API de TLS, pero tiene algunas desventajas.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="c3bc9-155">En primer lugar, Excel debe llamar **xlAutoFree**/ **xlAutoFree12** con independencia del tipo de devuelto **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="c3bc9-156">En segundo lugar, hay un problema cuando se devuelva **XLOPER**/ **XLOPER12**s que son el valor devuelto de una llamada a una función de devolución de llamada de la API de C.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12**s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="c3bc9-157">El **XLOPER**/ **XLOPER12** pueden señalar a la memoria que necesita ser liberados por Excel, pero el **XLOPER**/ se debe liberar**XLOPER12** propio de la misma manera se ha asignado.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="c3bc9-158">Si una de esas **XLOPER**/ **XLOPER12** es para usarse como el valor devuelto de una función de hoja de cálculo XLL, no hay ninguna forma sencilla de informar a **xlAutoFree**/ **xlAutoFree12** de la necesidad de liberar ambos punteros de la manera adecuada.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="c3bc9-159">(El establecimiento de la **xlbitXLFree** y **xlbitDLLFree** no soluciona el problema, como el tratamiento de **XLOPER/XLOPER12s** en Excel con ambos set no está definido y puede cambiar de una versión a otra.) Para evitar este problema, el XLL puede realizar copias en profundidad de todos los asignados Excel **XLOPER/XLOPER12s** que devuelve a la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="c3bc9-160">Una solución que evita estas limitaciones es rellenar y devolver un subproceso local **XLOPER y XLOPER12**, un método que requiere que **xlAutoFree/xlAutoFree12** que no la libera el puntero **XLOPER y XLOPER12** propio.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
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

<span data-ttu-id="c3bc9-161">La siguiente pregunta es cómo configurar y recuperar la memoria local de subprocesos, en otras palabras, cómo implementar la función **get_thread_local_xloper12** en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-161">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example.</span></span> <span data-ttu-id="c3bc9-162">Esto se realiza mediante el subproceso almacenamiento Local (TLS) API.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-162">This is done using the Thread Local Storage (TLS) API.</span></span> <span data-ttu-id="c3bc9-163">El primer paso es obtener un índice TLS mediante **TlsAlloc**, que finalmente se deben liberar mediante **TlsFree**.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-163">The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**.</span></span> <span data-ttu-id="c3bc9-164">Ambos se realizan mejor desde **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-164">Both are best accomplished from **DllMain**.</span></span>
  
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

<span data-ttu-id="c3bc9-165">Después de obtener el índice, el siguiente paso es asignar un bloque de memoria para cada subproceso.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-165">After you obtain the index, the next step is to allocate a block of memory for each thread.</span></span> <span data-ttu-id="c3bc9-166">La [Documentación de desarrollo de Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) se recomienda hacer esto cada vez que se llama a la función de devolución de llamada de **DllMain** con un evento **DLL_THREAD_ATTACH** y liberar la memoria en cada **DLL_THREAD_DETACH**.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-166">The [Windows Development Documentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**.</span></span> <span data-ttu-id="c3bc9-167">Sin embargo, siga este Consejo hará que el archivo DLL realizar el trabajo innecesario para subprocesos que no se usan para el recálculo.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-167">However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="c3bc9-168">En su lugar, es mejor usar una estrategia de asignación en primer uso.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-168">Instead, it is better to use an allocate-on-first-use strategy.</span></span> <span data-ttu-id="c3bc9-169">En primer lugar, debe definir una estructura que se va a asignar a cada proceso.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-169">First, you need to define a structure that you want to allocate for each thread.</span></span> <span data-ttu-id="c3bc9-170">Para los ejemplos anteriores que devuelven **XLOPER** o **XLOPER12s**, será suficiente, pero puede crear cualquier estructura que satisfaga sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-170">For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="c3bc9-171">La siguiente función obtiene un puntero a la instancia local de subprocesos, o asigna uno si se trata de la primera llamada.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
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

<span data-ttu-id="c3bc9-172">Ahora puede ver cómo se obtiene la memoria **XLOPER y XLOPER12** local de subproceso: en primer lugar, obtenga un puntero a la instancia del subproceso de **TLS_data**y, a continuación, se devuelve un puntero a la **XLOPER y XLOPER12** contenidos dentro de él, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
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

<span data-ttu-id="c3bc9-173">Las funciones **mtr_safe_example_1** y **mtr_safe_example_2** pueden estar registradas como funciones de hoja de cálculo seguros para subprocesos cuando se ejecutan Excel.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-173">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel.</span></span> <span data-ttu-id="c3bc9-174">Sin embargo, no puede mezclar los dos enfoques en un XLL.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-174">However, you cannot mix the two approaches in one XLL.</span></span> <span data-ttu-id="c3bc9-175">Su XLL sólo puede exportar una implementación de **xlAutoFree** y **xlAutoFree12**, y cada estrategia de memoria requiere un enfoque diferente.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-175">Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach.</span></span> <span data-ttu-id="c3bc9-176">Con **mtr_safe_example_1**, se debe liberar el puntero pasado a **xlAutoFree/xlAutoFree12** junto con los datos que señale a.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-176">With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to.</span></span> <span data-ttu-id="c3bc9-177">Con **mtr_safe_example_2**, se deben liberar sólo los datos que apunta a.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-177">With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="c3bc9-178">Windows también proporciona una función **GetCurrentThreadId**, que devuelve el identificador único para todo el sistema. del subproceso actual</span><span class="sxs-lookup"><span data-stu-id="c3bc9-178">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID.</span></span> <span data-ttu-id="c3bc9-179">Esto proporciona el programador con otra forma para que el subproceso de código segura, o para hacer que su subproceso de comportamiento específico.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-179">This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="c3bc9-180">Memoria accesible sólo mediante más de un subproceso: secciones críticas</span><span class="sxs-lookup"><span data-stu-id="c3bc9-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="c3bc9-181">Debe proteger la memoria de lectura y escritura que puede tener acceso a más de un subproceso mediante secciones críticas.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-181">You should protect read/write memory that can be accessed by more than one thread using critical sections.</span></span> <span data-ttu-id="c3bc9-182">Necesita una sección crítica con nombre para cada bloque de memoria que desea proteger.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-182">You need a named critical section for each block of memory you want to protect.</span></span> <span data-ttu-id="c3bc9-183">Puede inicializar durante la llamada a la función **xlAutoOpen** y liberarlos y establezca en null durante la llamada a la función **xlAutoClose** .</span><span class="sxs-lookup"><span data-stu-id="c3bc9-183">You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function.</span></span> <span data-ttu-id="c3bc9-184">A continuación, debe contener cada acceso al bloque protegido dentro de un par de llamadas a **EnterCriticalSection** y **LeaveCriticalSection**.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-184">You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**.</span></span> <span data-ttu-id="c3bc9-185">Sólo un subproceso está permitido en la sección crítica en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-185">Only one thread is permitted into the critical section at any time.</span></span> <span data-ttu-id="c3bc9-186">Este es un ejemplo de la inicialización, desinicialización y uso de una sección denominada **g_csSharedTable**.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-186">Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
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

<span data-ttu-id="c3bc9-187">Tal vez más seguro, otra forma de proteger un bloque de memoria es crear una clase que contiene su propia **CRITICAL_SECTION** y cuyo constructor, destructor y los métodos de descriptor de acceso se encargan de su uso.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-187">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use.</span></span> <span data-ttu-id="c3bc9-188">Este enfoque tiene la ventaja de protección de objetos que se pueden inicializar antes de **xlAutoOpen** se ejecuta o sobrevivir después de llamar a **xlAutoClose** , pero debe tener cuidado acerca de la creación de un número excesivo de las secciones críticas y el sistema operativo sobrecarga de la que esto crearía.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-188">This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="c3bc9-189">Cuando haya código que necesita tener acceso a más de un bloque de memoria protegida al mismo tiempo, debe tener en cuenta el orden en que las secciones críticas entran y salen de cuidadosamente.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-189">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited.</span></span> <span data-ttu-id="c3bc9-190">Por ejemplo, las dos funciones siguientes podrían crear un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-190">For example, the following two functions could create a deadlock.</span></span>
  
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

<span data-ttu-id="c3bc9-191">Si la primera función en un subproceso entra en el **g_csSharedTableA** mientras entra en el segundo en otro subproceso **g_csSharedTableB**, ambos procesos se bloquean.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-191">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang.</span></span> <span data-ttu-id="c3bc9-192">El enfoque correcto es escribe en un orden coherente y la salida en el orden inverso, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-192">The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="c3bc9-193">Siempre que sea posible, es mejor desde un subproceso cooperación punto de vista para aislar el acceso a distintos bloques, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
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

<span data-ttu-id="c3bc9-194">Donde hay una gran cantidad de contención para un recurso compartido, como las solicitudes de acceso frecuente de corta duración, considere la posibilidad de uso de capacidad de la sección crítica para girar.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-194">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin.</span></span> <span data-ttu-id="c3bc9-195">Ésta es una técnica que pone en espera para el recurso menos intensivos del procesador.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-195">This is a technique that makes waiting for the resource less processor-intensive.</span></span> <span data-ttu-id="c3bc9-196">Para ello, puede utilizar cualquiera **InitializeCriticalSectionAndSpinCount** al inicializar la sección o **SetCriticalSectionSpinCount** una vez inicializada, para establecer el número de veces que el subproceso realiza un bucle antes de esperar para convertirse en los recursos de se encuentra disponible.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-196">To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available.</span></span> <span data-ttu-id="c3bc9-197">La operación de espera es cara, por lo que girando Esto evita si el recurso se libera muchísimo.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-197">The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime.</span></span> <span data-ttu-id="c3bc9-198">En un sistema de procesador único, el número de recombinaciones de forma eficaz se pasa por alto, pero aún se puede especificar sin problemas.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-198">On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm.</span></span> <span data-ttu-id="c3bc9-199">El administrador del montón de memoria usa un recuento de rotación de 4000.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-199">The memory heap manager uses a spin count of 4000.</span></span> <span data-ttu-id="c3bc9-200">Para obtener más información acerca del uso de secciones críticas, consulte la documentación del SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="c3bc9-200">For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c3bc9-201">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3bc9-201">See also</span></span>



[<span data-ttu-id="c3bc9-202">Administración de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="c3bc9-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="c3bc9-203">Actualización multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="c3bc9-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="c3bc9-204">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="c3bc9-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

