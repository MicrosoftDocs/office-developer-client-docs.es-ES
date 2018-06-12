---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- función xlAutoFree [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a2d2b8e60b484ba8156acc80d543493e3ec9c564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815721"
---
# <a name="xlautofreexlautofree12"></a><span data-ttu-id="f7ee4-104">xlAutoFree/xlAutoFree12</span><span class="sxs-lookup"><span data-stu-id="f7ee4-104">xlAutoFree/xlAutoFree12</span></span>

 <span data-ttu-id="f7ee4-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7ee4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f7ee4-106">Microsoft Excel llama justo después de que una función de hoja de cálculo XLL devuelve un **XLOPER**/ **XLOPER12** a ella con un conjunto de marca que indica que hay que sigue necesitando el XLL para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-106">Called by Microsoft Excel just after an XLL worksheet function returns an **XLOPER**/ **XLOPER12** to it with a flag set that tells it there is memory that the XLL still needs to release.</span></span> <span data-ttu-id="f7ee4-107">Esto permite que el XLL devolver dinámicamente asignado matrices, cadenas y las referencias externas a la hoja de cálculo sin pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-107">This enables the XLL to return dynamically allocated arrays, strings, and external references to the worksheet without memory leaks.</span></span> <span data-ttu-id="f7ee4-108">Para obtener m�s informaci�n, consulte [Administraci�n de memoria en Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="f7ee4-108">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="f7ee4-109">Iniciar en Excel 2007, la función **xlAutoFree12** y el tipo de datos **XLOPER12** son compatibles.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-109">Starting in Excel 2007, the **xlAutoFree12** function and the **XLOPER12** data type are supported.</span></span> 
  
<span data-ttu-id="f7ee4-110">Excel no requiere un XLL implementar y exportar a cualquiera de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-110">Excel does not require an XLL to implement and export either of these functions.</span></span> <span data-ttu-id="f7ee4-111">Sin embargo, debe hacerlo si sus funciones XLL devuelven un XLOPER o XLOPER12 que se han asignado dinámicamente o que contiene punteros a memoria asignada dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-111">However, you must do so if your XLL functions return an XLOPER or XLOPER12 that has been dynamically allocated or that contains pointers to dynamically allocated memory.</span></span> <span data-ttu-id="f7ee4-112">Asegúrese de que su elección de cómo administrar la memoria de estos tipos es coherente en toda su XLL y con cómo implementa **xlAutoFree** y **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-112">Ensure that your choice of how to manage memory for these types is consistent throughout your XLL and with how you implemented **xlAutoFree** and **xlAutoFree12**.</span></span>
  
<span data-ttu-id="f7ee4-113">Dentro de la **xlAutoFree**/ **xlAutoFree12** función, las devoluciones de llamada en Excel están deshabilitadas, con una excepción: puede llamarse a **xlFree** para liberar memoria asignada en Excel.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-113">Inside the **xlAutoFree**/ **xlAutoFree12** function, callbacks into Excel are disabled, with one exception: **xlFree** can be called to free Excel-allocated memory.</span></span> 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a><span data-ttu-id="f7ee4-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7ee4-114">Parameters</span></span>

 <span data-ttu-id="f7ee4-115">_pxFree_ (**LPXLOPER en el caso de xlAutoFree**)</span><span class="sxs-lookup"><span data-stu-id="f7ee4-115">_pxFree_ (**LPXLOPER in the case of xlAutoFree**)</span></span>
  
 <span data-ttu-id="f7ee4-116">_pxFree_ (**LPXLOPER12 en el caso de xlAutoFree12**)</span><span class="sxs-lookup"><span data-stu-id="f7ee4-116">_pxFree_ (**LPXLOPER12 in the case of xlAutoFree12**)</span></span>
  
<span data-ttu-id="f7ee4-117">Un puntero a la **XLOPER** o **XLOPER12** que tiene memoria que necesita ser liberados.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-117">A pointer to the **XLOPER** or the **XLOPER12** that has memory that needs to be freed.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f7ee4-118">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7ee4-118">Property value/Return value</span></span>

<span data-ttu-id="f7ee4-119">Esta función no devuelve un valor y se debe declarar como devolver void.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-119">This function does not return a value and should be declared as returning void.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7ee4-120">Notas</span><span class="sxs-lookup"><span data-stu-id="f7ee4-120">Remarks</span></span>

<span data-ttu-id="f7ee4-121">Cuando Excel está configurado para usar el nuevo cálculo multiproceso libro, **xlAutoFree**/ **xlAutoFree12** se llama en el mismo subproceso utilizado para llamar a la función que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-121">When Excel is configured to use multithreaded workbook recalculation, **xlAutoFree**/ **xlAutoFree12** is called on the same thread used to call the function that returned it.</span></span> <span data-ttu-id="f7ee4-122">La llamada a **xlAutoFree**/ **xlAutoFree12** siempre se realiza antes de que todas las celdas de la hoja de cálculo subsiguientes se evalúan en ese subproceso.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-122">The call to **xlAutoFree**/ **xlAutoFree12** is always made before any subsequent worksheet cells are evaluated on that thread.</span></span> <span data-ttu-id="f7ee4-123">Esto simplifica el diseño de subprocesos en su XLL.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-123">This simplifies thread-safe design in your XLL.</span></span> 
  
<span data-ttu-id="f7ee4-124">Si el **xlAutoFree**/ función**xlAutoFree12** proporciona examina el campo **xltype** de _pxFree_, recuerde que aún se establecerá el bit **xlbitDLLFree** .</span><span class="sxs-lookup"><span data-stu-id="f7ee4-124">If the **xlAutoFree**/ **xlAutoFree12** function you provide looks at the **xltype** field of  _pxFree_, remember that the **xlbitDLLFree** bit will still be set.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f7ee4-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7ee4-125">Example</span></span>

 <span data-ttu-id="f7ee4-126">**Implementación de ejemplo 1**</span><span class="sxs-lookup"><span data-stu-id="f7ee4-126">**Example Implementation 1**</span></span>
  
<span data-ttu-id="f7ee4-127">El primer código de `\SAMPLES\EXAMPLE\EXAMPLE.C` , se muestra una implementación muy específica de **xlAutoFree**, que está diseñado para funcionar con una sola función, **fArray**.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-127">The first code from  `\SAMPLES\EXAMPLE\EXAMPLE.C` demonstrates a very specific implementation of **xlAutoFree**, which is designed to work with just one function, **fArray**.</span></span> <span data-ttu-id="f7ee4-128">En general, su XLL tendrá más de un función de devolución de memoria que necesita liberarse, en cuyo caso se requiere una implementación menos restringida.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-128">In general, your XLL will have more than just one function returning memory that needs to be freed, in which case a less restricted implementation is required.</span></span> 
  
 <span data-ttu-id="f7ee4-129">**Implementación de ejemplo 2**</span><span class="sxs-lookup"><span data-stu-id="f7ee4-129">**Example implementation 2**</span></span>
  
<span data-ttu-id="f7ee4-130">El segundo ejemplo de implementación es coherente con los supuestos utilizados en los ejemplos de creación de **XLOPER12** en sección 1.6.3, xl12_Str_example, xl12_Ref_example y xl12_Multi_example.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-130">The second example implementation is consistent with the assumptions used in the **XLOPER12** creation examples in section 1.6.3, xl12_Str_example, xl12_Ref_example, and xl12_Multi_example.</span></span> <span data-ttu-id="f7ee4-131">Los supuestos son, cuando el bit **xlbitDLLFree** ha sido conjunto, todas las cadena, matriz y memoria de referencia externa se ha asignado dinámicamente utilizando **malloc**y, por tanto, debe ser liberados en una llamada a libre.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-131">The assumptions are that, when the **xlbitDLLFree** bit has been set, all string, array, and external reference memory has been dynamically allocated using **malloc**, and so needs to be freed in a call to free.</span></span>
  
 <span data-ttu-id="f7ee4-132">**Implementación de ejemplo 3**</span><span class="sxs-lookup"><span data-stu-id="f7ee4-132">**Example implementation 3**</span></span>
  
<span data-ttu-id="f7ee4-133">El tercer ejemplo de implementación es coherente con un XLL donde exportado las funciones que devuelven **XLOPER12**s asignan cadenas, las referencias externas y las matrices mediante **malloc**, y se asigna también dinámicamente **XLOPER12** propio.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-133">The third example implementation is consistent with an XLL where exported functions that return **XLOPER12**s allocate strings, external references and arrays using **malloc**, and where the **XLOPER12** itself is also dynamically allocated.</span></span> <span data-ttu-id="f7ee4-134">Devolución de un puntero a asignados dinámicamente **XLOPER12** es una forma de garantizar que la función es segura para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f7ee4-134">Returning a pointer to a dynamically allocated **XLOPER12** is one way to ensure that the function is thread safe.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="f7ee4-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="f7ee4-135">See also</span></span>



[<span data-ttu-id="f7ee4-136">Administrador de complementos y funciones de la interfaz XLL</span><span class="sxs-lookup"><span data-stu-id="f7ee4-136">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

