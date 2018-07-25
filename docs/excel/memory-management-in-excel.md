---
title: Administración de memoria en Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- xloper12 memory [excel 2007],managing memory in Excel,Excel stack,strings [Excel 2007], managing memory,memory management in Excel,XLOPER memory [Excel 2007],memory [Excel 2007], management guidelines
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97c76d762fdc5e575c571804816e5581a7bec8bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815691"
---
# <a name="memory-management-in-excel"></a><span data-ttu-id="cc92c-104">Administración de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="cc92c-104">Memory Management in Excel</span></span>

 <span data-ttu-id="cc92c-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cc92c-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cc92c-p101">La administración de memoria es la mayor preocupación si quiere crear XLL eficaces y estables. Si no se administra bien la memoria, pueden surgir una serie de problemas en Microsoft Excel: desde pequeños problemas, como una asignación e inicialización de memoria ineficiente y pequeñas pérdidas de memoria, hasta problemas importantes, como la desestabilización de Excel.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p101">Memory management is the most important concern if you want to create efficient and stable XLLs. Failure to manage memory well can lead to a range of problems in Microsoft Excel—from minor problems such as inefficient memory allocation and initialization and small memory leaks, to major problems such as the destabilization of Excel.</span></span>
  
<span data-ttu-id="cc92c-p102">Una mala administración de memoria es el origen más común de los problemas relacionados con complementos. Por lo tanto, debe compilar el proyecto con una estrategia coherente y bien planeada a través de la administración de memoria.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p102">Mismanagement of memory is the most common source of serious add-in-related problems. Therefore, you should build your project with a consistent and well-thought-through strategy on memory management.</span></span> 
  
<span data-ttu-id="cc92c-p103">La administración de memoria es más compleja en Microsoft Office Excel 2007 gracias a la Introducción de las actualizaciones de los libros multiproceso. Si quiere crear y exportar funciones de hoja de cálculo seguras para subprocesos, debe administrar los conflictos resultantes que se pueden producir cuando varios subprocesos compiten por el acceso.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p103">Memory management became more complex in Microsoft Office Excel 2007 with the introduction of multithreaded workbook recalculation. If you want to create and export thread-safe worksheet functions, you must manage the resulting conflicts that can occur when multiple threads compete for access.</span></span>
  
<span data-ttu-id="cc92c-112">Existen consideraciones de memoria para los siguientes tres tipos de estructura de datos:</span><span class="sxs-lookup"><span data-stu-id="cc92c-112">There are memory considerations for the following three data structure types:</span></span>
  
- <span data-ttu-id="cc92c-113">**XLOPER** y **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="cc92c-113">**XLOPER**s and **XLOPER12**s</span></span>
    
- <span data-ttu-id="cc92c-114">Cadenas que no se encuentran en **XLOPER** o **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="cc92c-114">Strings that are not in an **XLOPER** or **XLOPER12**</span></span>
    
- <span data-ttu-id="cc92c-115">Matrices de **FP** y **FP12**</span><span class="sxs-lookup"><span data-stu-id="cc92c-115">**FP** and **FP12** arrays</span></span> 
    
## <a name="xloperxloper12-memory"></a><span data-ttu-id="cc92c-116">Memoria XLOPER y XLOPER12</span><span class="sxs-lookup"><span data-stu-id="cc92c-116">XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="cc92c-117">La estructura de datos **XLOPER**/ **XLOPER12** tiene algunos subtipos que contienen punteros a bloques de memoria, concretamente cadenas (**xltypeStr**), matrices (**xltypeMulti**) y referencias externas (**xltypeRef**).</span><span class="sxs-lookup"><span data-stu-id="cc92c-117">The XLOPER/XLOPER12 data structure has a few sub-types that contain pointers to blocks of memory, namely strings (xltypeStr), arrays (xltypeMulti) and external references (xltypeRef). Note also that xltypeMulti arrays can contain string XLOPER/XLOPER12s that in turn point to other blocks of memory.</span></span> <span data-ttu-id="cc92c-118">Tenga en cuenta que las matrices **xltypeMulti** pueden contener cadenas **XLOPER**/ **XLOPER12s** que apuntan a su vez a otros bloques de memoria.</span><span class="sxs-lookup"><span data-stu-id="cc92c-118">Note also that **xltypeMulti** arrays can contain string **XLOPER**/ **XLOPER12s** that in turn point to other blocks of memory.</span></span> 
  
<span data-ttu-id="cc92c-119">Un **XLOPER**/ **XLOPER12** puede crearse de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="cc92c-119">An XLOPER/XLOPER12 can be created in several ways:</span></span> 
  
- <span data-ttu-id="cc92c-120">Mediante Excel al preparar los argumentos para pasarlos a una función XLL</span><span class="sxs-lookup"><span data-stu-id="cc92c-120">By Excel when preparing arguments to be passed to an XLL function</span></span>
    
- <span data-ttu-id="cc92c-121">Mediante Excel al devolver **XLOPER** o **XLOPER12** en una llamada a la API de C</span><span class="sxs-lookup"><span data-stu-id="cc92c-121">By Excel when returning an **XLOPER** or **XLOPER12** in a C API call</span></span> 
    
- <span data-ttu-id="cc92c-122">Mediante el DLL al crear los argumentos para pasarlos a la llamada de la API de C</span><span class="sxs-lookup"><span data-stu-id="cc92c-122">By your DLL when creating arguments to be passed to a C API call</span></span>
    
- <span data-ttu-id="cc92c-123">Mediante el DLL al crear un valor devuelto de la función XLL</span><span class="sxs-lookup"><span data-stu-id="cc92c-123">By your DLL when creating an XLL function return value</span></span>
    
<span data-ttu-id="cc92c-124">Se puede asignar un bloque de memoria en uno de los tipos que apuntan a memoria de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="cc92c-124">A block of memory within one of the memory-pointing types can be allocated in several ways:</span></span>
  
- <span data-ttu-id="cc92c-125">Puede ser un bloque estático dentro del DLL fuera de cualquier código de la función, en cuyo caso no tiene que asignar o liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="cc92c-125">It can be a static block within your DLL outside any function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="cc92c-126">Puede ser un bloque estático dentro del DLL dentro de algún código de la función, en cuyo caso no tiene que asignar o liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="cc92c-126">It can be a static block within your DLL within some function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="cc92c-127">El DLL puede asignarlo y liberarlo de forma din�mica de distintas formas: **malloc** y **free**, **new** y **delete**, etc.</span><span class="sxs-lookup"><span data-stu-id="cc92c-127">It can be dynamically allocated and freed by your DLL in several possible ways: **malloc** and **free**, **new** and **delete**, and so on.</span></span>
    
- <span data-ttu-id="cc92c-128">Excel puede asignarlo de forma dinámica.</span><span class="sxs-lookup"><span data-stu-id="cc92c-128">It can be dynamically allocated by Excel.</span></span>
    
<span data-ttu-id="cc92c-129">Dado el número de posibles orígenes de la memoria **XLOPER**/ **XLOPER12** y el número de situaciones en las que **XLOPER**/ **XLOPER12** pueden tener memoria asignada, no es sorprendente que este asunto pueda parecer difícil.</span><span class="sxs-lookup"><span data-stu-id="cc92c-129">Given the number of possible origins for XLOPER/XLOPER12 memory and the number of situations in which the XLOPER/XLOPER12 might have had that memory assigned, it is not surprising that this subject can seem very difficult. However, the complexity can be greatly reduced if you follow several rules and guidelines.</span></span> <span data-ttu-id="cc92c-130">Sin embargo, la complejidad se puede reducir en gran medida si sigue varias instrucciones y reglas.</span><span class="sxs-lookup"><span data-stu-id="cc92c-130">However, the complexity can be greatly reduced if you follow several rules and guidelines.</span></span> 
  
### <a name="rules-for-working-with-xloperxloper12"></a><span data-ttu-id="cc92c-131">Reglas para trabajar con XLOPER y XLOPER12</span><span class="sxs-lookup"><span data-stu-id="cc92c-131">Rules for Working with XLOPER/XLOPER12</span></span>

- <span data-ttu-id="cc92c-132">No intente liberar memoria ni sobrescribir **XLOPER**/ **XLOPER12** que se pasan como argumentos a la función XLL.</span><span class="sxs-lookup"><span data-stu-id="cc92c-132">Do not try to free memory or overwrite **XLOPERs**/ **XLOPER12**s that are passed as arguments to your XLL function.</span></span> <span data-ttu-id="cc92c-133">Debe tratar dichos argumentos como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc92c-133">You should treat such arguments as read-only.</span></span> <span data-ttu-id="cc92c-134">Para obtener más información, vea "Devolver **XLOPER** o **XLOPER12** modificando argumentos locales" en [Problemas conocidos del desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="cc92c-134">For more information, see "Returning **XLOPER** or **XLOPER12** by Modifying Arguments in Place" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
    
- <span data-ttu-id="cc92c-135">Si Excel asigna memoria para un **XLOPER**/ **XLOPER12** devuelto al DLL en una llamada a la API de C:</span><span class="sxs-lookup"><span data-stu-id="cc92c-135">If Excel has allocated memory for an XLOPER/XLOPER12 returned to your DLL in a call to the C API:</span></span> 
    
  - <span data-ttu-id="cc92c-136">Debe liberar la memoria cuando ya no necesita el **XLOPER**/ **XLOPER12** mediante una llamada a [xlFree](xlfree.md).</span><span class="sxs-lookup"><span data-stu-id="cc92c-136">You must free the memory when you no longer need the XLOPER/XLOPER12 using a call to xlFree. Do not use any other method, such as free or delete, to release the memory.</span></span> <span data-ttu-id="cc92c-137">No use cualquier otro método, como liberar ni eliminar, para liberar la memoria.</span><span class="sxs-lookup"><span data-stu-id="cc92c-137">You must free the memory when you no longer need the XLOPER/XLOPER12 using a call to xlFree. Do not use any other method, such as free or delete, to release the memory.</span></span>
    
  - <span data-ttu-id="cc92c-138">Si el tipo devuelto es **xltypeMulti**, no sobrescriba ningún **XLOPER**/ **XLOPER12** dentro de la matriz, especialmente si contienen cadenas, y especialmente no donde intenta sobrescribir con una cadena.</span><span class="sxs-lookup"><span data-stu-id="cc92c-138">If the returned type is xltypeMulti, do not overwrite any XLOPER/XLOPER12s within the array, especially if they contain strings, and especially not where you are trying to overwrite with a string.</span></span>
    
  - <span data-ttu-id="cc92c-139">Si quiere devolver **XLOPER**/ **XLOPER12** a Excel como valor devuelto de la función de DLL, debe indicarle a Excel que hay memoria que debe liberar al terminar.</span><span class="sxs-lookup"><span data-stu-id="cc92c-139">If you want to return the XLOPER/XLOPER12 to Excel as your DLL function’s return value, you must tell Excel that there is memory that Excel must release when done.</span></span> 
    
- <span data-ttu-id="cc92c-140">Solo debe llamar **xlFree** en **XLOPER**/ **XLOPER12** creado como el valor devuelto para una llamada a la API de C.</span><span class="sxs-lookup"><span data-stu-id="cc92c-140">You must only call xlFree on an XLOPER/XLOPER12 that was created as the return value to a C API call.</span></span> 
    
- <span data-ttu-id="cc92c-141">Si el DLL asigna memoria para **XLOPER**/ **XLOPER12** que quiere devolver a Excel como valor devuelto de la función de DLL, debe indicarle a Excel que hay memoria que DLL debe liberar.</span><span class="sxs-lookup"><span data-stu-id="cc92c-141">If your DLL has allocated memory for an XLOPER/XLOPER12 that you want to return to Excel as your DLL function’s return value, you must tell Excel that there is memory that the DLL must release.</span></span> 
    
### <a name="guidelines-for-memory-management"></a><span data-ttu-id="cc92c-142">Directrices para la administración de memoria</span><span class="sxs-lookup"><span data-stu-id="cc92c-142">Guidelines for Memory Management</span></span>

- <span data-ttu-id="cc92c-p108">Sea coherente en el DLL del método que usa para asignar y liberar memoria. Evite mezclar métodos. Un buen enfoque es ajustar el método que use en una clase o estructura de memoria, en el que puede cambiar el método usado sin alterar el código en muchos lugares.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p108">Be consistent in your DLL in the method that you use to allocate and release memory. Avoid mixing methods. A good approach is to wrap the method that you are using up in a memory class or structure, within which you can change the method used without altering your code in many places.</span></span>
    
- <span data-ttu-id="cc92c-p109">Al crear matrices de **xltypeMulti** dentro del DLL, sea coherente en la forma en que asigna memoria para las cadenas: asigne siempre din�micamente la memoria para ellos o use siempre la memoria est�tica. Para ello, al liberar memoria, sabr� que debe liberar siempre o nunca las cadenas.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p109">When you create **xltypeMulti** arrays within your DLL, be consistent in the way that you allocate memory for strings: always dynamically allocate the memory for them or always use static memory. If you do this, when you are freeing the memory, you will know that you must either always or never free the strings.</span></span> 
    
- <span data-ttu-id="cc92c-148">Haga copias en profundidad de memoria asignada a Excel al copiar un **XLOPER**/ **XLOPER12** creado en Excel.</span><span class="sxs-lookup"><span data-stu-id="cc92c-148">Make deep copies of Excel-allocated memory when you are copying an Excel-created XLOPER/XLOPER12.</span></span>
    
- <span data-ttu-id="cc92c-149">No incluya cadenas asignadas a Excel **XLOPER**/ **XLOPER12** dentro de las matrices de **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-149">Do not put Excel-allocated string **XLOPER**/ **XLOPER12**s within **xltypeMulti** arrays.</span></span> <span data-ttu-id="cc92c-150">Haga copias en profundidad de las cadenas y los punteros de almacenamiento para las copias de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cc92c-150">Do not put Excel-allocated string XLOPER/XLOPER12s within xltypeMulti arrays. Make deep copies of the strings and store pointers to the copies in the array.</span></span> 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a><span data-ttu-id="cc92c-151">Liberar memoria XLOPER o XLOPER12 asignada a Excel</span><span class="sxs-lookup"><span data-stu-id="cc92c-151">Freeing Excel-Allocated XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="cc92c-152">Tenga en cuenta el siguiente comando XLL que usa **xlGetName** para obtener una cadena que contenga la ruta de acceso y el nombre del DLL y que los muestra en un cuadro de di�logo de alerta con **xlcAlert**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-152">Consider the following XLL command, which uses **xlGetName** to obtain a string containing the path and file name of the DLL and displays it in an alert dialog box using **xlcAlert**.</span></span>
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

<span data-ttu-id="cc92c-153">Cuando la función ya no necesita la memoria a la que **xDllName** apunta, puede liberarla con una llamada a la [función xlFree](xlfree.md), una de las funciones de la API de C solo de DLL.</span><span class="sxs-lookup"><span data-stu-id="cc92c-153">When the function no longer needs the memory pointed to by **xDllName**, it can free it using a call to the [xlFree function](xlfree.md), one of the DLL-only C API functions.</span></span> 
  
<span data-ttu-id="cc92c-154">La función **xlFree** se documenta en la secci�n de referencia de la función (consulte [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), pero tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc92c-154">The **xlFree** function is fully documented in the function reference section (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), but be aware of the following:</span></span>
  
- <span data-ttu-id="cc92c-155">Puede pasar punteros a más de un **XLOPER**/ **XLOPER12** en una sola llamada a **xlFree**, limitado solo por el número de argumentos de función admitidos en la versión en ejecución de Excel (30 en Excel 2003, 255 a partir de Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="cc92c-155">You can pass pointers to more than one XLOPER/XLOPER12s in a single call to xlFree, limited only by the number of function arguments supported in the running version of Excel (30 in Excel 2003, 255 starting in xlxlshort).</span></span>
    
- <span data-ttu-id="cc92c-156">**xlFree** configura el puntero contenido en **NULL** para asegurarse de que un intento de liberar **XLOPER**/ **XLOPER12** que ya se ha liberado es seguro.</span><span class="sxs-lookup"><span data-stu-id="cc92c-156">xlFree sets the contained pointer to NULL to ensure that an attempt to free an XLOPER/XLOPER12 that has already been freed is safe. xlFree is the only C API function that modifies its arguments.</span></span> <span data-ttu-id="cc92c-157">**xlFree** es la única función de la API de C que modifica los argumentos.</span><span class="sxs-lookup"><span data-stu-id="cc92c-157">**xlFree** is the only C API function that modifies its arguments.</span></span> 
    
- <span data-ttu-id="cc92c-158">Puede llamar de forma segura a **xlFree** en cualquier **XLOPER**/ **XLOPER12** usado para el valor devuelto de una llamada a la API de C, independientemente de si contiene un puntero a la memoria.</span><span class="sxs-lookup"><span data-stu-id="cc92c-158">You can safely call xlFree on any XLOPER/XLOPER12 used for the return value of a call to the C API, regardless of whether it contains a pointer to memory.</span></span> 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a><span data-ttu-id="cc92c-159">Devolver XLOPER o XLOPER12 para que Excel los libere</span><span class="sxs-lookup"><span data-stu-id="cc92c-159">Returning XLOPER/XLOPER12s to be freed by Excel</span></span>

<span data-ttu-id="cc92c-160">Suponga que desea modificar el comando de ejemplo en la sección anterior y lo cambia a una función de hoja de cálculo que devuelve el nombre de archivo y la ruta DLL cuando pasa un argumento **verdadero** **booleano** y **#N/A** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cc92c-160">Suppose you wanted to modify the example command in the previous section and change it to a worksheet function that returns the DLL path and file name when passed a **Boolean** **true** argument, and **#N/A** otherwise.</span></span> <span data-ttu-id="cc92c-161">Evidentemente no puede llamar a **xlFree** para liberar la memoria de cadena antes de devolverla a Excel.</span><span class="sxs-lookup"><span data-stu-id="cc92c-161">Clearly you cannot call **xlFree** to release the string memory before returning it to Excel.</span></span> <span data-ttu-id="cc92c-162">Sin embargo, si no se ha liberado en algún momento, el complemento pierde memoria cada vez que se llama a la función.</span><span class="sxs-lookup"><span data-stu-id="cc92c-162">However, if it is not freed at some point, the add-in will leak memory every time the function is called.</span></span> <span data-ttu-id="cc92c-163">Para solucionar este problema, puede establecer un bit en el campo **xltype** del **XLOPER**/ **XLOPER12**, definido como **xlbitXLFree** en xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="cc92c-163">To work around this problem, you can set a bit in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitXLFree** in xlcall.h.</span></span> <span data-ttu-id="cc92c-164">Esta configuración le indica a Excel que debe liberar la memoria devuelta cuando ha terminado de copiar el valor.</span><span class="sxs-lookup"><span data-stu-id="cc92c-164">Setting this tells Excel that it must free the returned memory when it has finished copying the value out.</span></span> 
  
### <a name="example"></a><span data-ttu-id="cc92c-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc92c-165">Example</span></span>

<span data-ttu-id="cc92c-166">En el siguiente ejemplo de código se muestra el comando XLL de la sección anterior convertido en una función de hoja de cálculo XLL.</span><span class="sxs-lookup"><span data-stu-id="cc92c-166">The following code example shows the XLL command in the previous section converted into an XLL worksheet function.</span></span>
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

<span data-ttu-id="cc92c-167">Las funciones de XLL que usan **XLOPER**/ **XLOPER12** deben declararse como que toman y devuelven punteros a **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-167">XLL functions that use **XLOPER**/ **XLOPER12**s must be declared as taking and returning pointers to **XLOPER**/ **XLOPER12**s.</span></span> <span data-ttu-id="cc92c-168">El uso en este ejemplo de un **XLOPER12** estático dentro de la función no es seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="cc92c-168">The use in this example of a static **XLOPER12** within the function is not thread safe.</span></span> <span data-ttu-id="cc92c-169">Puede registrar incorrectamente esta función como segura para subprocesos, pero correría el riesgo de que un subproceso sobrescriba **xRtnValue** antes de que otro haya terminado de usarlo.</span><span class="sxs-lookup"><span data-stu-id="cc92c-169">XLL functions that use **XLOPER**/XLOPER12s must be declared as taking and returning pointers to XLOPER/XLOPER12s. The use in this example of a static XLOPER12 within the function is not thread safe. You could incorrectly register this function as thread safe, but you would risk xRtnValue being overwritten by one thread before another thread had finished with it.</span></span> 
  
<span data-ttu-id="cc92c-170">Debe establecer **xlbitXLFree** después de la llamada a la devolución de llamada de Excel que lo asigna.</span><span class="sxs-lookup"><span data-stu-id="cc92c-170">You must set **xlbitXLFree** after the call to the Excel callback that allocates it.</span></span> <span data-ttu-id="cc92c-171">Si lo establece antes de esta, se sobrescribe y no tiene el efecto deseado.</span><span class="sxs-lookup"><span data-stu-id="cc92c-171">If you set it before this, it is overwritten and does not have the effect that you want.</span></span> <span data-ttu-id="cc92c-172">Si desea usar el valor como un argumento en una llamada a otra función de la API de C antes de volver a la hoja de cálculo, debe establecer este bit después de cualquier llamada.</span><span class="sxs-lookup"><span data-stu-id="cc92c-172">If you intend to use the value as an argument in a call to another C API function before returning it to the worksheet, you should set this bit after any such call.</span></span> <span data-ttu-id="cc92c-173">En caso contrario, confundirá las funciones que no lo enmascaran poco antes de proteger el tipo **XLOPER**/ **XLLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-173">Otherwise, you will confuse functions that do not mask this bit before checking the **XLOPER**/ **XLLOPER12** type.</span></span> 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a><span data-ttu-id="cc92c-174">Devolver XLOPER o XLOPER12 para que el DLL los libere</span><span class="sxs-lookup"><span data-stu-id="cc92c-174">Returning XLOPER/XLOPER12s to be freed by the DLL</span></span>

<span data-ttu-id="cc92c-175">Un problema similar a este se produce cuando el XLL ha asignado memoria para un **XLOPER**/ **XLOPER12** y desea devolverla a Excel.</span><span class="sxs-lookup"><span data-stu-id="cc92c-175">A similar problem to this occurs when your XLL has allocated memory for an XLOPER/XLOPER12 and wants to return it to Excel. Excel recognizes another bit that can be set in the xltype field of the XLOPER/XLOPER12, defined as xlbitDLLFree in xlcall.h.</span></span> <span data-ttu-id="cc92c-176">Excel reconoce otro bit que se puede establecer en el campo **xltype** del **XLOPER**/ **XLOPER12**, definido como un **xlbitDLLFree** en xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="cc92c-176">A similar problem to this occurs when your XLL has allocated memory for an XLOPER/XLOPER12 and wants to return it to Excel. Excel recognizes another bit that can be set in the xltype field of the XLOPER/XLOPER12, defined as xlbitDLLFree in xlcall.h.</span></span> 
  
<span data-ttu-id="cc92c-177">Cuando Excel recibe **un XLOPER**/ **XLOPER12** con este conjunto de bits, intenta llamar a una función que debería exportar el XLL denominado [xlAutoFree](xlautofree-xlautofree12.md) (para **XLOPER**) o **xlAutoFree12** (para **XLOPER12**).</span><span class="sxs-lookup"><span data-stu-id="cc92c-177">When Excel receives **an XLOPER**/ **XLOPER12** with this bit set, it tries to call a function that should be exported by the XLL called [xlAutoFree](xlautofree-xlautofree12.md) (for **XLOPER**s) or **xlAutoFree12** (for **XLOPER12**s).</span></span> <span data-ttu-id="cc92c-178">Esta función se describe más detalladamente en la referencia de la función (vea [Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)), pero aquí se proporciona una implementación mínima.</span><span class="sxs-lookup"><span data-stu-id="cc92c-178">This function is described more fully in the function reference (see [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)), but an example minimal implementation is given here.</span></span> <span data-ttu-id="cc92c-179">Su objetivo es liberar la memoria de **XLOPER**/ **XLOPER12** de forma coherente con la que se asignó originalmente.</span><span class="sxs-lookup"><span data-stu-id="cc92c-179">Its purpose is to free the **XLOPER**/ **XLOPER12** memory in a way that is consistent with how it was originally allocated.</span></span> 
  
### <a name="examples"></a><span data-ttu-id="cc92c-180">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cc92c-180">Examples</span></span>

<span data-ttu-id="cc92c-181">La siguiente función del ejemplo realiza lo mismo que la función anterior excepto en que incluye el texto "El nombre de la ruta de acceso completa de este DLL es" delante del nombre del DLL.</span><span class="sxs-lookup"><span data-stu-id="cc92c-181">The following example function does the same as the previous function except that it includes the text "The full pathname for this DLL is " before the DLL name.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

<span data-ttu-id="cc92c-182">Una implementaci�n m�nima suficiente de **xlAutoFree12** en el XLL que exporta la función anterior ser�a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="cc92c-182">A minimally sufficient implementation of **xlAutoFree12** in the XLL that exported the previous function would be as follows.</span></span> 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

<span data-ttu-id="cc92c-p117">Esta implementaci�n solo es suficiente si el XLL solo devuelve la cadena **XLOPER12** y estas cadenas solo se asignan con **malloc**. Tenga en cuenta que la prueba</span><span class="sxs-lookup"><span data-stu-id="cc92c-p117">This implementation is only sufficient if the XLL only returns **XLOPER12** strings, and those strings are only allocated using **malloc**. Note that the test</span></span> 
  
 ` if(p_oper->xltype == xltypeStr) `
  
<span data-ttu-id="cc92c-185">producir� un error en este caso porque **xlbitDLLFree** est� configurado.</span><span class="sxs-lookup"><span data-stu-id="cc92c-185">would fail in this case because **xlbitDLLFree** is set.</span></span> 
  
<span data-ttu-id="cc92c-186">En general, **xlAutoFree** y **xlAutoFree12** se deben implementar para que liberen la memoria asociada con las matrices de **xltypeMulti** creadas con XLL y las referencias externas de **xltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-186">In general, **xlAutoFree** and **xlAutoFree12** should be implemented so that they free memory associated with XLL-created **xltypeMulti** arrays and **xltypeRef** external references.</span></span> 
  
<span data-ttu-id="cc92c-187">Puede decidir implementar sus funciones XLL para que todas devuelvan **XLOPER** y **XLOPER12** asignados dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="cc92c-187">You might decide to implement your XLL functions so that they ALL return dynamically allocated **XLOPER**s and **XLOPER12**s.</span></span> <span data-ttu-id="cc92c-188">En este caso, debe configurar **xlbitDLLFree** en todos los **XLOPER** y **XLOPER12** independientemente del tipo secundario.</span><span class="sxs-lookup"><span data-stu-id="cc92c-188">In this case, you would need to set **xlbitDLLFree** on all such **XLOPER**s and **XLOPER12**s regardless of the sub-type.</span></span> <span data-ttu-id="cc92c-189">También necesitará implementar **xlAutoFree** y **xlAutoFree12** para que se libere esta memoria y también cualquier memoria a la que se apunta dentro del **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-189">You would also need to implement **xlAutoFree** and **xlAutoFree12** so that this memory was freed and also any memory pointed to within the **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="cc92c-190">Este método es una forma de hacer el valor de la conversación devuelto seguro.</span><span class="sxs-lookup"><span data-stu-id="cc92c-190">This approach is one way to make the return value thread safe.</span></span> <span data-ttu-id="cc92c-191">Por ejemplo, la función anterior podría modificarse como se indica.</span><span class="sxs-lookup"><span data-stu-id="cc92c-191">For example, the previous function could be rewritten as follows.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

<span data-ttu-id="cc92c-192">Para obtener m�s información de **xlAutoFree** y **xlAutoFree12**, consulte [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span><span class="sxs-lookup"><span data-stu-id="cc92c-192">For more information about **xlAutoFree** and **xlAutoFree12**, see [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span></span>
  
## <a name="returning-modify-in-place-arguments"></a><span data-ttu-id="cc92c-193">Devolver argumentos Modificación local</span><span class="sxs-lookup"><span data-stu-id="cc92c-193">Returning Modify-in-Place Arguments</span></span>

<span data-ttu-id="cc92c-p119">Excel permite que una función XLL devuelva un valor modificando un argumento local. Solo se puede hacer con un argumento que se pasa como puntero. Para que funcione así, se debe registrar la función de modo que indique a Excel el argumento que se modificará.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p119">Excel allows an XLL function to return a value by modifying an argument in place. You can only do this with an argument passed in as a pointer. To work like this, the function must be registered in a way that tells Excel which argument will be modified.</span></span> 
  
<span data-ttu-id="cc92c-197">Este método de devolución de un valor se admite con todos los tipos de datos que el puntero puede pasar, pero es especialmente útil para los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="cc92c-197">This method of returning a value is supported for all data types that can be passed by pointer but is especially useful for the following types:</span></span>
  
- <span data-ttu-id="cc92c-198">Cadenas de bytes ASCII de longitud contada y terminada en valor nulo</span><span class="sxs-lookup"><span data-stu-id="cc92c-198">Length-counted and null-terminated ASCII byte strings</span></span>
    
- <span data-ttu-id="cc92c-199">Cadenas de caracteres anchos Unicode de longitud contada y terminada en valor nulo (a partir de Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="cc92c-199">Length-counted and null-terminated Unicode wide character strings (starting in Excel 2007)</span></span>
    
- <span data-ttu-id="cc92c-200">Matrices **FP** de n�mero de punto flotante</span><span class="sxs-lookup"><span data-stu-id="cc92c-200">**FP** floating-point arrays</span></span> 
    
- <span data-ttu-id="cc92c-201">Matrices **FP12**de n�mero de punto flotante (a partir de Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="cc92c-201">**FP12** floating-point arrays (starting in Excel 2007)</span></span> 
    
> [!NOTE]
> <span data-ttu-id="cc92c-p120">No debe intentar devolver **XLOPER** o **XLOPER12** de este modo. Para obtener m�s información, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="cc92c-p120">You should not try to return **XLOPER**s or **XLOPER12**s in this manner. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span> 
  
<span data-ttu-id="cc92c-p121">La ventaja de usar esta técnica, en lugar de solo usar la instrucción return, es que Excel asigna la memoria para los valores devueltos. Una vez que termina la lectura de los datos devueltos, libera la memoria. Esto aleja las tareas de administración de memoria de la función XLL. Esta técnica es segura para subprocesos: si Excel lo llama simultáneamente en subprocesos distintos, cada llamada a la función de cada subproceso tiene su propio búfer.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p121">The advantage of using this technique, instead of just using the return statement, is that Excel allocates the memory for the return values. Once Excel has finished reading the returned data, it releases the memory. This takes the memory management tasks away from the XLL function. This technique is thread safe: If called concurrently by Excel on different threads, each function call on each thread has its own buffer.</span></span>
  
<span data-ttu-id="cc92c-208">Es útil para los datos enumerados anteriormente, en particular porque el mecanismo de devolución de llamada al DLL para liberar memoria posterior a la devolución que existe para **XLOPER**/ **XLOPER12** no existe para las cadenas simples y las matrices de **FP**/ **FP12**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-208">It is useful for the previously listed data types in particular because the mechanism for calling back into the DLL to free memory post-return that exists for XLOPER/XLOPER12s does not exist for simple strings and FP/FP12 arrays. Therefore, when returning a DLL-created string or floating-point array, you have the following choices:</span></span> <span data-ttu-id="cc92c-209">Por lo tanto, al devolver una cadena creada por DLL o una matriz de número de punto flotante, tiene las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="cc92c-209">Therefore, when returning a DLL-created string or floating-point array, you have the following choices:</span></span> 
  
- <span data-ttu-id="cc92c-p123">Configurar un puntero persistente para un búfer asignado dinámicamente, devolver el puntero. En la siguiente llamada a la función (1) compruebe que el puntero no sea nulo, (2) libre los recursos asignados en la llamada anterior y restablezca el puntero a nulo, (3) reutilice el puntero para un bloque de memoria asignado recientemente.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p123">Set a persistent pointer to a dynamically allocated buffer, return the pointer. On the next call to the function (1) check that the pointer is not null, (2) free the resources allocated on the previous call and reset the pointer to null, (3) reuse the pointer for a newly allocated block of memory.</span></span>
    
- <span data-ttu-id="cc92c-212">Crear las cadenas y las matrices en un búfer estático que no se tenga que liberar y devolver un puntero.</span><span class="sxs-lookup"><span data-stu-id="cc92c-212">Create your strings and arrays in a static buffer that does not need to be freed, and return a pointer to that.</span></span>
    
- <span data-ttu-id="cc92c-213">Modificar un argumento local, escribiendo la cadena o la matriz directamente en el espacio reservado por Excel.</span><span class="sxs-lookup"><span data-stu-id="cc92c-213">Modify an argument in place, writing your string or array directly into the space set aside by Excel.</span></span>
    
<span data-ttu-id="cc92c-214">De lo contrario, debe crear un **XLOPER**/ **XLOPER12**, y usar **xlbitDLLFree** y **xlAutoFree**/ **xlAutoFree12** para liberar los recursos.</span><span class="sxs-lookup"><span data-stu-id="cc92c-214">Otherwise, you must create an XLOPER/XLOPER12, and use xlbitDLLFree and xlAutoFree/xlAutoFree12 to release the resources.</span></span> 
  
<span data-ttu-id="cc92c-215">La última opción puede ser la más sencilla en los casos en los que se pasa un argumento del mismo tipo como el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="cc92c-215">The last option might be the simplest in those cases in which you are being passed an argument of the same type as the return value.</span></span> <span data-ttu-id="cc92c-216">El punto clave que debe recordar es que se limitan los tamaños de búfer y debe tener mucho cuidado de no saturarlos.</span><span class="sxs-lookup"><span data-stu-id="cc92c-216">The key point to remember is that the buffer sizes are limited and you must be very careful not to overrun them.</span></span> <span data-ttu-id="cc92c-217">Hacerlo de forma incorrecta puede llevar a que se bloquee Excel.</span><span class="sxs-lookup"><span data-stu-id="cc92c-217">Getting this wrong could crash Excel.</span></span> <span data-ttu-id="cc92c-218">Los tamaños de búfer de las cadenas y las matrices **FP**/ **FP12** se describen a continuación.</span><span class="sxs-lookup"><span data-stu-id="cc92c-218">Buffer sizes for strings and **FP**/ **FP12** arrays are discussed next.</span></span> 
  
## <a name="strings"></a><span data-ttu-id="cc92c-219">Strings</span><span class="sxs-lookup"><span data-stu-id="cc92c-219">Strings</span></span>

<span data-ttu-id="cc92c-220">Los problemas con la administración de la memoria de la cadena son probablemente la causa más común de inestabilidad en las aplicaciones y los complementos. Quizá es comprensible dadas las diversas formas en las que se gestionan las cadenas: terminada en null o longitud contada (o ambos); búferes estáticos o dinámicos; longitud fija o casi ilimitada; memoria administrada por el sistema operativo (por ejemplo, OLE Bstr) o cadenas no administradas, etc.</span><span class="sxs-lookup"><span data-stu-id="cc92c-220">Problems with the management of string memory are arguably the most common cause of instability in applications and add-ins. It is understandable perhaps, given the variety of ways in which strings are handled: null-terminated or length-counted (or both); static or dynamic buffers; fixed length or almost unlimited length; operating-system managed memory (for example, OLE Bstr) or unmanaged strings; and so on.</span></span>
  
<span data-ttu-id="cc92c-p125">Los programadores de C/C ++ están más familiarizados con las cadenas terminada en null. La biblioteca estándar de C está diseñada para trabajar con estas cadenas. Los literales de cadena estática del código se compilan en cadenas terminadas en null. Como alternativa, Excel funciona con cadenas de longitud contada que normalmente no están terminadas en null. La combinación de estos hechos necesita un enfoque claro y coherente dentro de la DLL o  XLL sobre cómo gestionar las cadenas y la memoria de la cadena.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p125">C/C++ programmers are most familiar with null-terminated strings. The standard C library is designed to work with such strings. Static string literals in code are compiled into null-terminated strings. Alternatively, Excel works with length-counted strings that are not in general null-terminated. The combination of these facts requires a clear and consistent approach within your DLL/XLL regarding how you handle strings and string memory.</span></span>
  
<span data-ttu-id="cc92c-226">Los problemas más comunes son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cc92c-226">The most common problems are as follows:</span></span>
  
- <span data-ttu-id="cc92c-227">Pasar un puntero nulo o no v�lido a una función que espera un puntero v�lido y no tiene o no puede comprobar la validez del puntero.</span><span class="sxs-lookup"><span data-stu-id="cc92c-227">The passing of a null or invalid pointer to a function that expects a valid pointer and does not or cannot check the pointer's validity itself.</span></span>
    
- <span data-ttu-id="cc92c-228">Saturar los límites de un búfer de cadena por una función que no tiene o no puede comprobar la longitud del búfer con la longitud de la cadena que se escribe.</span><span class="sxs-lookup"><span data-stu-id="cc92c-228">The overrunning of the bounds of a string buffer by a function that does not or cannot check the length of the buffer against the length of the string being written.</span></span>
    
- <span data-ttu-id="cc92c-229">Intentar liberar la memoria de búfer de cadena que es estática, que ya se ha liberado o no se ha asignado de forma coherente con la forma en que se libera.</span><span class="sxs-lookup"><span data-stu-id="cc92c-229">Trying to free string buffer memory that is either static, or has been freed already, or was not allocated in a way that is consistent with how it is being freed.</span></span>
    
- <span data-ttu-id="cc92c-230">Pérdidas de memoria que son el resultado de las cadenas que se asignan y que no se liberan, normalmente en una función a la que se llama con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="cc92c-230">Memory leaks that result from strings being allocated and then not freed, usually in a frequently called function.</span></span>
    
### <a name="rules-for-strings"></a><span data-ttu-id="cc92c-231">Reglas para las cadenas</span><span class="sxs-lookup"><span data-stu-id="cc92c-231">Rules for Strings</span></span>

<span data-ttu-id="cc92c-232">Al igual que con los **XLOPER**/ **XLOPER**, hay reglas e instrucciones que debe seguir.</span><span class="sxs-lookup"><span data-stu-id="cc92c-232">As with **XLOPER**/ **XLOPER**s, there are rules and guidelines you should follow.</span></span> <span data-ttu-id="cc92c-233">Las instrucciones son las mismas que las indicadas en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="cc92c-233">The guidelines are the same as given in the previous section.</span></span> <span data-ttu-id="cc92c-234">Las reglas que se presentan aquí son una extensión de las reglas específicas para las cadenas.</span><span class="sxs-lookup"><span data-stu-id="cc92c-234">The rules here are an extension of the rules specifically for strings.</span></span>
  
 <span data-ttu-id="cc92c-235">**Reglas:**</span><span class="sxs-lookup"><span data-stu-id="cc92c-235">**Rules:**</span></span>
  
- <span data-ttu-id="cc92c-236">No intente liberar memoria o sobrescribir **XLOPER**/ **XLOPER12** de cadena, o cadenas de longitud contada simples o terminadas en null que se pasan como argumentos para la función XLL.</span><span class="sxs-lookup"><span data-stu-id="cc92c-236">Do not try to free memory or overwrite string XLOPER/XLOPER12s or simple length-counted or null-terminated strings passed as arguments to your XLL function. You should treat such arguments as read-only.</span></span> <span data-ttu-id="cc92c-237">Debe tratar dichos argumentos como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cc92c-237">You should treat such arguments as read-only.</span></span>
    
- <span data-ttu-id="cc92c-238">Cuando Excel asigna memoria para**XLOPER**/ **XLOPER12** de cadena para el valor devuelto de una función de devolución de llamada de la API de C, use **xlFree** para liberarla, o configure **xlbitXLFree** si la devuelve a Excel desde una función XLL.</span><span class="sxs-lookup"><span data-stu-id="cc92c-238">Where Excel allocates memory for a string XLOPER/XLOPER12 for the return value of a C API callback function, use xlFree to free it, or set xlbitXLFree if returning it to Excel from an XLL function.</span></span> 
    
- <span data-ttu-id="cc92c-239">Cuando el DLL asigna dinámicamente un búfer de cadena para **XLOPER**/ **XLOPER12**, libérelo de forma coherente con la forma en la que lo asignó, o configure **xlbitDLLFree** si lo devuelve a Excel desde una función XLL y libérelo en **xlAutoFree**/ **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-239">Where your DLL dynamically allocates a string buffer for an XLOPER/XLOPER12, free it in a way consistent with how you allocated it when done, or set xlbitDLLFree if returning it to Excel from an XLL function and then free it in xlAutoFree/xlAutoFree12.</span></span>
    
- <span data-ttu-id="cc92c-240">Si Excel ha asignado la memoria para una matriz **xltypeMulti** devuelta al DLL en una llamada a la API de C, no sobrescriba cualquier cadena **XLOPER**/ **XLOPER12** dentro de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cc92c-240">If Excel has allocated memory for an xltypeMulti array returned to your DLL in a call to the C API, do not overwrite any string XLOPER/XLOPER12s within the array. Such arrays must only be freed using xlFree, or, if being returned by an XLL function, by setting xlbitXLFree.</span></span> <span data-ttu-id="cc92c-241">Estas matrices solo deben liberarse mediante **xlFree**, o bien, si las devuelve una función XLL, estableciendo **xlbitXLFree**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-241">Such arrays must only be freed using **xlFree**, or, if being returned by an XLL function, by setting **xlbitXLFree**.</span></span>
    
### <a name="string-types-supported"></a><span data-ttu-id="cc92c-242">Tipos de cadena admitidos</span><span class="sxs-lookup"><span data-stu-id="cc92c-242">String Types Supported</span></span>

<span data-ttu-id="cc92c-243">**XLOPER o XLOPER12 de xltypeStr de la API de C**</span><span class="sxs-lookup"><span data-stu-id="cc92c-243">**C API xltypeStr XLOPER/XLOPER12s**</span></span>

|<span data-ttu-id="cc92c-244">**Cadenas de bytes: **XLOPER****</span><span class="sxs-lookup"><span data-stu-id="cc92c-244">**Byte strings: **XLOPER****</span></span>|<span data-ttu-id="cc92c-245">**Cadenas de caracteres anchos: **XLOPER12****</span><span class="sxs-lookup"><span data-stu-id="cc92c-245">**Wide character strings: **XLOPER12****</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc92c-246">Todas las versiones de Excel</span><span class="sxs-lookup"><span data-stu-id="cc92c-246">All versions of Excel</span></span>  <br/> |<span data-ttu-id="cc92c-247">A partir de Excel 2007</span><span class="sxs-lookup"><span data-stu-id="cc92c-247">Starting in Excel 2007</span></span>  <br/> |
|<span data-ttu-id="cc92c-248">Longitud máxima: 255 caracteres ASCII ampliados</span><span class="sxs-lookup"><span data-stu-id="cc92c-248">Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="cc92c-249">Longitud máxima 32.767 caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="cc92c-249">Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="cc92c-250">Primer byte (no asignado) = longitud</span><span class="sxs-lookup"><span data-stu-id="cc92c-250">First (unsigned) byte = length</span></span>  <br/> |<span data-ttu-id="cc92c-251">Primer carácter Unicode = longitud</span><span class="sxs-lookup"><span data-stu-id="cc92c-251">First Unicode character = length</span></span>  <br/> |
   
> [!IMPORTANT]
> <span data-ttu-id="cc92c-252">No asuma la terminaci�n null de las cadenas **XLOPER** o **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-252">Do not assume null termination of **XLOPER** or **XLOPER12** strings.</span></span> 
  
<span data-ttu-id="cc92c-253">**Cadenas C/C++**</span><span class="sxs-lookup"><span data-stu-id="cc92c-253">**C/C++ strings**</span></span>

|<span data-ttu-id="cc92c-254">**Cadenas de bytes**</span><span class="sxs-lookup"><span data-stu-id="cc92c-254">**Byte strings**</span></span>|<span data-ttu-id="cc92c-255">**Cadenas de caracteres anchos**</span><span class="sxs-lookup"><span data-stu-id="cc92c-255">**Wide character strings**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc92c-256">Longitud máxima de "C" terminada en null (**char** \*): 255 bytes ASCII ampliados</span><span class="sxs-lookup"><span data-stu-id="cc92c-256">Null-terminated (**char** \*) "C" Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="cc92c-257">Longitud máxima "C%" terminada en null (**wchar_t** \*) 32 767 caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="cc92c-257">Null-terminated (**wchar_t** \*) "C%" Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="cc92c-258">"D" de longitud contada (**unsigned char** \*)</span><span class="sxs-lookup"><span data-stu-id="cc92c-258">Length-counted (**unsigned char** \*) "D"</span></span>  <br/> |<span data-ttu-id="cc92c-259">"% D" de longitud contada (**wchar_t** \*)</span><span class="sxs-lookup"><span data-stu-id="cc92c-259">Length-counted (**wchar_t** \*) "D%"</span></span>  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a><span data-ttu-id="cc92c-260">Cadenas de las matrices XLOPER o XLOPER12 de xltypeMulti</span><span class="sxs-lookup"><span data-stu-id="cc92c-260">Strings in xltypeMulti XLOPER/XLOPER12 Arrays</span></span>

<span data-ttu-id="cc92c-p129">En muchos casos, Excel crea una matriz **xltypeMulti** para su uso en los XLL o DLL. Varias de las funciones de información XLM devuelven estas matrices. Por ejemplo, la función de la API de C **xlfGetWorkspace**, cuando pasa el argumento  *44*  , devuelve una matriz que contiene las cadenas que describen todos los procedimientos DLL registrados actualmente. La función de la API de C **xlfDialogBox** devuelve una copia modificada del argumento de la matriz, que contiene copias en profundidad de las cadenas. Posiblemente, el modo m�s com�n en que un XLL encuentra una matriz de **xltypeMulti** es donde se ha pasado como argumento a una función XLL, o se ha forzado para este tipo desde una referencia de rango. En estos �ltimos casos, Excel crea copias en profundidad de las cadenas en las celdas de origen y apunta a estos dentro de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p129">In several cases, Excel creates an **xltypeMulti** array for use in your DLL/XLL. Several of the XLM information functions return such arrays. For example, the C API function **xlfGetWorkspace**, when passed the argument  *44*  , returns an array containing strings that describe all the currently registered DLL procedures. The C API function **xlfDialogBox** returns a modified copy of its array argument, containing deep copies of the strings. Perhaps the most common way an XLL encounters an **xltypeMulti** array is where it has been passed as an argument to an XLL function, or it has been coerced to this type from a range reference. In these latter cases, Excel creates deep copies of the strings in the source cells and points to these within the array.</span></span> 
  
<span data-ttu-id="cc92c-267">Debe hacer sus propias copias en profundidad donde desee modificar estas cadenas en el DLL.</span><span class="sxs-lookup"><span data-stu-id="cc92c-267">Where you want to modify these strings in your DLL, you should make your own deep copies.</span></span> <span data-ttu-id="cc92c-268">Al crear su propias matrices **xltypeMulti**, no debe colocar las cadenas asignadas a Excel **XLOPER**/ **XLOPER12** en ellas.</span><span class="sxs-lookup"><span data-stu-id="cc92c-268">When you are creating your own **xltypeMulti** arrays, you should not place Excel-allocated string **XLOPER**/ **XLOPER12**s within them.</span></span> <span data-ttu-id="cc92c-269">Hacer esto implica el riesgo de no liberarlas correctamente más adelante, o no liberarlas en absoluto.</span><span class="sxs-lookup"><span data-stu-id="cc92c-269">This risks you not freeing them correctly later, or not freeing them at all.</span></span> <span data-ttu-id="cc92c-270">De nuevo, debe hacer copias en profundidad de las cadenas y los punteros de almacenamiento para las copias de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cc92c-270">Again, you should make deep copies of the strings and store pointers to the copies in the array.</span></span>
  
 <span data-ttu-id="cc92c-271">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="cc92c-271">**Examples**</span></span>
  
<span data-ttu-id="cc92c-p131">La siguiente función del ejemplo crea una copia asignada din�micamente de una cadena Unicode de longitud contada. Tenga en cuenta que, en �ltima instancia, el llamador debe liberar la memoria asignada en este ejemplo con **delete**[], y que no se supone que la cadena de origen termine en null. La cadena de copia se trunca si es necesario por motivos de seguridad y no termina en null.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p131">The following example function creates a dynamically allocated copy of a length-counted Unicode string. Note that the caller must ultimately free the memory allocated in this example using **delete**[], and that the source string is not assumed to be null terminated. The copy string is truncated if necessary for safety, and is not null terminated.</span></span>
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

<span data-ttu-id="cc92c-p132">Luego, esta función se puede usar con seguridad para copiar **XLOPER12**, como se muestra en la siguiente función XLL que se puede exportar y que devuelve una copia de su argumento, si es una cadena. El resto de tipos se devuelve como una cadena de longitud cero. Tenga en cuenta que no se gestionan los rangos; la función devuelve **#VALUE!**. se debe registrar la función como que toma un argumento de tipo U, de modo que las referencias se pasen como valores. Esto es igual a la función de hoja de cálculo integrada **T()**, excepto en que **AsText** tambi�n convierte los errores en cadenas de longitud cero. Este ejemplo de códigoasume que **xlAutoFree12** libera el puntero pasado, y tambi�n su contenido, con **delete**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p132">This function can then be safely used to copy an **XLOPER12**, as shown in the following exportable XLL function that returns a copy of its argument if it is a string. All other types are returned as a zero-length string. Note that ranges are not handled—the function returns **#VALUE!**. The function must be registered as taking a type U argument so that references are passed in as values. This is equivalent to the built-in worksheet function **T()** except that **AsText** also converts errors to zero-length strings. This code example assumes that **xlAutoFree12** frees the passed-in pointer, and also its contents, using **delete**.</span></span>
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a><span data-ttu-id="cc92c-281">Devolver argumentos de cadena Modificación local</span><span class="sxs-lookup"><span data-stu-id="cc92c-281">Returning Modify-in-Place String Arguments</span></span>

<span data-ttu-id="cc92c-p133">Los argumentos registrados como tipos **F**, **G**, **F%** y **G%** se pueden modificar de forma local. Cuando Excel prepara argumentos de cadena para estos tipos, se crea un b�fer de longitud m�xima. Luego, copia la cadena del argumento en �l, incluso si esta cadena es mucho m�s corta. Esto permite que la función XLL escriba el valor devuelto directamente en la misma memoria.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p133">Arguments registered as types **F**, **G**, **F%**, and **G%** can be modified in place. When Excel is preparing string arguments for these types, it creates a maximum length buffer. Then it copies the argument string into that, even if this string is very much shorter. This enables the XLL function to write its return value directly into the same memory.</span></span> 
  
<span data-ttu-id="cc92c-286">Los tamaños de búfer configurados aparte para estos tipos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cc92c-286">Buffer sizes set apart for these types are as follows:</span></span>
  
- <span data-ttu-id="cc92c-287">**Cadenas de bytes:** 256 bytes, incluido el contador de longitud (tipo G) o la terminaci�n null (tipo F).</span><span class="sxs-lookup"><span data-stu-id="cc92c-287">**Byte strings:** 256 bytes including the length counter (type G) or null-termination (type F).</span></span> 
    
- <span data-ttu-id="cc92c-288">**Cadenas Unicode:** 32.768 caracteres anchos (65.536 bytes), incluido el contador de longitud (tipo G%) o la terminaci�n null (tipo F%).</span><span class="sxs-lookup"><span data-stu-id="cc92c-288">**Unicode strings:** 32,768 wide characters (65,536 bytes) including the length counter (type G%) or null-termination (type F%).</span></span> 
    
> [!NOTE]
> <span data-ttu-id="cc92c-p134">No puede llamar a esta función directamente desde Visual Basic para aplicaciones (VBA) porque no puede garantizar que se haya asignado un búfer suficientemente grande. Solo puede llamar de forma segura a esta función desde otra DLL si pasa explícitamente un búfer lo suficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p134">You cannot call such a function directly from Visual Basic for Applications (VBA) because you cannot ensure that a sufficiently large buffer has been allocated. You can only call such a function from another DLL safely if you have explicitly passed a big enough buffer.</span></span> 
  
<span data-ttu-id="cc92c-p135">Este es un ejemplo de una función XLL que invierte una cadena de caracteres anchos terminada en null con la función de biblioteca est�ndar **wcsrev**. El argumento en este caso se registrar� como tipo **F%**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p135">Here is an example of an XLL function that reverses a passed-in null-terminated wide character string using the standard library function **wcsrev**. The argument in this case would be registered as type **F%**.</span></span>
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a><span data-ttu-id="cc92c-293">Almacenamiento persistente (nombres binarios)</span><span class="sxs-lookup"><span data-stu-id="cc92c-293">Persistent Storage (Binary Names)</span></span>

<span data-ttu-id="cc92c-294">Los nombres binarios se definen y asocian con bloques de archivos binarios, es decir, datos no estructurados almacenados con el libro.</span><span class="sxs-lookup"><span data-stu-id="cc92c-294">Binary names are defined and associated with blocks of binary, that is, unstructured, data that is stored together with the workbook.</span></span> <span data-ttu-id="cc92c-295">Se crean con la función [xlDefineBinaryName](xldefinebinaryname.md) y los datos se recuperan con la función [xlGetBinaryName](xlgetbinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="cc92c-295">They are created using the function [xlDefineBinaryName](xldefinebinaryname.md), and the data is retrieved using the function [xlGetBinaryName](xlgetbinaryname.md).</span></span> <span data-ttu-id="cc92c-296">Ambas funciones se describen con más detalle en la referencia de función (vea [Funciones de la API de C que pueden llamarse solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), y que usan el **XLOPER**/ **XLOPER12** **xltypeBigData**.</span><span class="sxs-lookup"><span data-stu-id="cc92c-296">Both functions are described in more detail in the function reference (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), and both use the **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> 
  
<span data-ttu-id="cc92c-297">Para obtener información sobre los problemas conocidos que limitan las aplicaciones pr�cticas de los nombres binarios, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="cc92c-297">For information about known issues that limit the practical applications of binary names, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="excel-stack"></a><span data-ttu-id="cc92c-298">Pila de Excel</span><span class="sxs-lookup"><span data-stu-id="cc92c-298">Excel Stack</span></span>

<span data-ttu-id="cc92c-p137">Excel comparte su espacio de pila con todos los DLL que tiene cargados. Normalmente, el espacio de pila es más adecuado para su uso normal y no es necesario preocuparse por él, siempre y cuando siga unas directrices:</span><span class="sxs-lookup"><span data-stu-id="cc92c-p137">Excel shares its stack space with all the DLLs it has loaded. Stack space is usually more than adequate for ordinary use, and you do not need to be concerned about it as long as you follow a few guidelines:</span></span> 
  
- <span data-ttu-id="cc92c-p138">No pase estructuras muy grandes como argumentos a funciones por valor de la pila. En su lugar, pase punteros o referencias.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p138">Do not pass very large structures as arguments to functions by value on the stack. Pass pointers or references instead.</span></span>
    
- <span data-ttu-id="cc92c-p139">No devuelva estructuras grandes en la pila. Devuelva punteros para la memoria estática o asignada dinámicamente, o use argumentos que pase la referencia.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p139">Do not return large structures on the stack. Return pointers to static or dynamically allocated memory, or use arguments passed by reference.</span></span>
    
- <span data-ttu-id="cc92c-p140">No declare estructuras de variables automáticas muy grandes al código de función. Si las necesita, declárelas como estáticos.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p140">Do not declare very large automatic variable structures in the function code. If you need them, declare them as static.</span></span>
    
- <span data-ttu-id="cc92c-p141">No llame a las funciones recursivamente a menos que esté seguro de que la profundidad de la recursividad sea siempre superficial. En su lugar, intente usar un bucle.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p141">Do not call functions recursively unless you are sure the depth of recursion will always be shallow. Try using a loop instead.</span></span>
    
<span data-ttu-id="cc92c-p142">Cuando un archivo DLL devuelve la llamada a Excel con la API de C, Excel comprueba primero si hay suficiente espacio en la pila para la peor llamada de uso que se pueda realizar. Si piensa que no puede haber espacio suficiente, la llamada no ser� segura, aunque sea posible que realmente haya suficiente espacio para esa llamada concreta. En este caso, las devoluciones de llamada devuelven el código**xlretFailed**. Para el uso normal de la API de C y la pila, esta no es una causa probable del error de una llamada a la API de C.</span><span class="sxs-lookup"><span data-stu-id="cc92c-p142">When a DLL calls back into Excel using the C API, Excel first checks whether there is enough space on the stack for the worst-case usage call that could be made. If it thinks there might be insufficient room, it will fail the call to be safe, even though there might actually have been enough space for that particular call. In this case, the callbacks return the code **xlretFailed**. For ordinary use of the C API and the stack, this is an unlikely cause of the failure of a C API call.</span></span>
  
<span data-ttu-id="cc92c-313">Si le preocupa o le interesa, quiere eliminar la falta de espacio de pila como un motivo de un error inesperado, puede averiguar cu�nto espacio de pila hay con una llamada a la función [xlStack](xlstack.md).</span><span class="sxs-lookup"><span data-stu-id="cc92c-313">If you are concerned, or just curious, or you want to eliminate lack of stack space as a reason for an unexplained failure, you can find out how much stack space there is with a call to the [xlStack](xlstack.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc92c-314">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc92c-314">See also</span></span>



[<span data-ttu-id="cc92c-315">Actualización multiproceso en Excel</span><span class="sxs-lookup"><span data-stu-id="cc92c-315">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="cc92c-316">Subprocesamiento m�ltiple y la contenci�n de memoria en Excel</span><span class="sxs-lookup"><span data-stu-id="cc92c-316">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
  
[<span data-ttu-id="cc92c-317">Desarrollo de XLL de Excel de 2013</span><span class="sxs-lookup"><span data-stu-id="cc92c-317">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

