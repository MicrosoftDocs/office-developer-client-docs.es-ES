---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- función xlautofree [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3dfba5ae98b0635c95308eac01bf2f10867678e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413293"
---
# <a name="xlautofreexlautofree12"></a><span data-ttu-id="e26b1-104">xlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="e26b1-104">xlAutoFree/xlAutoFree12</span></span>

 <span data-ttu-id="e26b1-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e26b1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e26b1-106">Llamado por Microsoft Excel justo después de que una función de hoja de cálculo XLL devuelva un /  **XLOPER XLOPER12** con un conjunto de marcas que le indica que hay memoria que el XLL aún necesita liberar.</span><span class="sxs-lookup"><span data-stu-id="e26b1-106">Called by Microsoft Excel just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** to it with a flag set that tells it there is memory that the XLL still needs to release.</span></span> <span data-ttu-id="e26b1-107">Esto permite al XLL devolver matrices, cadenas y referencias externas asignadas dinámicamente a la hoja de cálculo sin pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="e26b1-107">This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks.</span></span> <span data-ttu-id="e26b1-108">Para obtener más información, consulte [Administración de memoria en Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="e26b1-108">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="e26b1-109">A partir de Excel 2007, se admiten la función **xlAutoFree12** y el tipo de datos **XLOPER12.**</span><span class="sxs-lookup"><span data-stu-id="e26b1-109">Starting in Excel 2007, the **xlAutoFree12** function and the **XLOPER12** data type are supported.</span></span> 
  
<span data-ttu-id="e26b1-110">Excel no requiere un XLL para implementar y exportar ninguna de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="e26b1-110">Excel does not require an XLL to implement and export either of these functions.</span></span> <span data-ttu-id="e26b1-111">Sin embargo, debe hacerlo si las funciones XLL devuelven un XLOPER o XLOPER12 que se ha asignado dinámicamente o que contiene punteros a la memoria asignada dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="e26b1-111">However, you must do so if your XLL functions return an XLOPER or XLOPER12 that has been dynamically allocated or that contains pointers to dynamically allocated memory.</span></span> <span data-ttu-id="e26b1-112">Asegúrese de que la elección de cómo administrar la memoria para estos tipos es coherente en todo el XLL y en la forma en que implementó **xlAutoFree** y **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="e26b1-112">Ensure that your choice of how to manage memory for these types is consistent throughout your XLL and with how you implemented **xlAutoFree** and **xlAutoFree12**.</span></span>
  
<span data-ttu-id="e26b1-113">Dentro de la función **xlAutoFree** /  **xlAutoFree12,** las devoluciones de llamada a Excel están deshabilitadas, con una excepción: se puede llamar a **xlFree** para liberar memoria asignada a Excel.</span><span class="sxs-lookup"><span data-stu-id="e26b1-113">Inside the **xlAutoFree**/ **xlAutoFree12** function, callbacks into Excel are disabled, with one exception: **xlFree** can be called to free Excel-allocated memory.</span></span> 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a><span data-ttu-id="e26b1-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e26b1-114">Parameters</span></span>

 <span data-ttu-id="e26b1-115">_pxFree_ (**LPXLOPER en el caso de xlAutoFree**)</span><span class="sxs-lookup"><span data-stu-id="e26b1-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span></span>
  
 <span data-ttu-id="e26b1-116">_pxFree_ (**LPXLOPER12 en el caso de xlAutoFree12**)</span><span class="sxs-lookup"><span data-stu-id="e26b1-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span></span>
  
<span data-ttu-id="e26b1-117">Puntero a **XLOPER** o **XLOPER12** que tiene memoria que debe liberarse.</span><span class="sxs-lookup"><span data-stu-id="e26b1-117">A pointer to the **XLOPER** or the **XLOPER12** that has memory that needs to be freed.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e26b1-118">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e26b1-118">Property value/Return value</span></span>

<span data-ttu-id="e26b1-119">Esta función no devuelve un valor y debe declararse como nula de devolución.</span><span class="sxs-lookup"><span data-stu-id="e26b1-119">This function does not return a value and should be declared as returning void.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e26b1-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e26b1-120">Remarks</span></span>

<span data-ttu-id="e26b1-121">Cuando Excel está configurado para usar la actualización de libros multiproceso, se llama a **xlAutoFree** /  **xlAutoFree12** en el mismo subproceso usado para llamar a la función que la devolvió.</span><span class="sxs-lookup"><span data-stu-id="e26b1-121">When Excel is configured to use multithreaded workbook recalculation, **xlAutoFree**/ **xlAutoFree12** is called on the same thread used to call the function that returned it.</span></span> <span data-ttu-id="e26b1-122">La llamada a **xlAutoFree**/ **xlAutoFree12** siempre se realiza antes de que las celdas de la hoja de cálculo siguientes se evalúen en dicho subproceso.</span><span class="sxs-lookup"><span data-stu-id="e26b1-122">The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread.</span></span> <span data-ttu-id="e26b1-123">Esto simplifica el diseño de subprocesos seguros en tu XLL.</span><span class="sxs-lookup"><span data-stu-id="e26b1-123">This simplifies thread-safe design in your XLL.</span></span> 
  
<span data-ttu-id="e26b1-124">Si la **función xlAutoFree** /  **xlAutoFree12** que proporcionas examina el campo **xltype** de _pxFree,_ recuerda que el bit **xlbitDLLFree** seguirá estando establecido.</span><span class="sxs-lookup"><span data-stu-id="e26b1-124">If the **xlAutoFree**/ **xlAutoFree12** function you provide looks at the **xltype** field of  _pxFree_, remember that the **xlbitDLLFree** bit will still be set.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e26b1-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e26b1-125">Example</span></span>

 <span data-ttu-id="e26b1-126">**Ejemplo de implementación 1**</span><span class="sxs-lookup"><span data-stu-id="e26b1-126">**Example Implementation 1**</span></span>
  
<span data-ttu-id="e26b1-127">El primer código de muestra una implementación muy específica de xlAutoFree , que está diseñada para funcionar con una sola `\SAMPLES\EXAMPLE\EXAMPLE.C` función, **fArray**. </span><span class="sxs-lookup"><span data-stu-id="e26b1-127">The first code from  `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstrates a very specific implementation of **xlAutoFree**, which is designed to work with just one function, **fArray**.</span></span> <span data-ttu-id="e26b1-128">En general, el XLL tendrá más de una función que devuelve memoria que debe liberarse, en cuyo caso se requiere una implementación menos restringida.</span><span class="sxs-lookup"><span data-stu-id="e26b1-128">In general, your XLL will have more than just one function returning memory that needs to be freed, in which case a less restricted implementation is required.</span></span> 
  
 <span data-ttu-id="e26b1-129">**Ejemplo de implementación 2**</span><span class="sxs-lookup"><span data-stu-id="e26b1-129">**Example implementation 2**</span></span>
  
<span data-ttu-id="e26b1-130">La segunda implementación de ejemplo es coherente con las suposiciones usadas en los ejemplos de creación de **XLOPER12** de la sección 1.6.3, xl12_Str_example, xl12_Ref_example y xl12_Multi_example.</span><span class="sxs-lookup"><span data-stu-id="e26b1-130">The second example implementation is consistent with the assumptions used in the **XLOPER12** creation examples in section 1.6.3, xl12_Str_example, xl12_Ref_example, and xl12_Multi_example.</span></span> <span data-ttu-id="e26b1-131">Se supone que, cuando se ha establecido el bit **xlbitDLLFree,** toda la cadena, matriz y memoria de referencia externa se ha asignado dinámicamente mediante **malloc,** por lo que debe liberarse en una llamada para liberar.</span><span class="sxs-lookup"><span data-stu-id="e26b1-131">The assumptions are that, when the **xlbitDLLFree** bit has been set, all string, array, and external reference memory has been dynamically allocated using **malloc**, and so needs to be freed in a call to free.</span></span>
  
 <span data-ttu-id="e26b1-132">**Ejemplo de implementación 3**</span><span class="sxs-lookup"><span data-stu-id="e26b1-132">**Example implementation 3**</span></span>
  
<span data-ttu-id="e26b1-133">La tercera implementación de ejemplo es coherente con un XLL donde las funciones exportadas que devuelven **XLOPER12** asignan cadenas, referencias externas y matrices mediante **malloc,** y donde el propio **XLOPER12** también se asigna dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="e26b1-133">The third example implementation is consistent with an XLL where exported functions that return **XLOPER12** s allocate strings, external references and arrays using **malloc**, and where the **XLOPER12** itself is also dynamically allocated.</span></span> <span data-ttu-id="e26b1-134">Devolver un puntero a un **XLOPER12** asignado dinámicamente es una forma de garantizar que la función es segura para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="e26b1-134">Returning a pointer to a dynamically allocated **XLOPER12** is one way to ensure that the function is thread safe.</span></span> 
  
```cs
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 1
//////////////////////////////////////////
LPXLOPER12 WINAPI fArray(void)
{
    LPXLOPER12 pxArray;
    static XLOPER12 xMulti;
    int i;
    int rwcol;
    xMulti.xltype = xltypeMulti | xlbitDLLFree;
    xMulti.val.array.columns = 1;
    xMulti.val.array.rows = 8;
    // For large values of rows and columns, this would overflow
    // use __int64 in that case and return an error if rwcol
    // contains a number that won't fit in sizeof(int) bytes
    rwcol = xMulti.val.array.columns * xMulti.val.array.rows; 
    pxArray = (LPXLOPER12)GlobalLock(hArray = GlobalAlloc(GMEM_ZEROINIT, rwcol * sizeof(XLOPER12)));
    xMulti.val.array.lparray = pxArray;
    for(i = 0; i < rwcol; i++) 
    {
        pxArray[i].xltype = xltypeInt;
        pxArray[i].val.w = i;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe, use alternate memory allocation mechanisms
    return (LPXLOPER12)&xMulti;
}
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    GlobalUnlock(hArray);
    GlobalFree(hArray);
    return;
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 2
//////////////////////////////////////////
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
/* Assume all string elements were allocated using malloc, and
** need to be freed using free.  Then free the array itself.
*/
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 3
//////////////////////////////////////////
LPXLOPER12 WINAPI example_xll_function(LPXLOPER12 pxArg)
{
// Thread-safe return value. Every invocation of this function
// gets its own piece of memory.
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
// Initialize to a safe default
    pxRtnValue->xltype = xltypeNil;
// Set the value of pxRtnValue making sure that strings, external
// references, arrays, and strings within arrays are all dynamically
// allocated using malloc.
//    (code omitted)
//    ...
// Set xlbitDLLFree regardless of the type of the return value to
// ensure xlAutoFree12 is called and pxRtnValue is freed.
    pxRtnValue->xltype |= xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
// Assume all string elements were allocated using malloc, and
// need to be freed using free. Then free the array itself.
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
// Assume pxFree was itself dynamically allocated using malloc.
    free(pxFree);
}
```

## <a name="see-also"></a><span data-ttu-id="e26b1-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e26b1-135">See also</span></span>



[<span data-ttu-id="e26b1-136">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="e26b1-136">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

