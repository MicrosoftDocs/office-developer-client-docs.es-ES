---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- función xlset [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404606"
---
# <a name="xlset"></a><span data-ttu-id="6efea-104">xlSet</span><span class="sxs-lookup"><span data-stu-id="6efea-104">xlSet</span></span>

<span data-ttu-id="6efea-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6efea-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6efea-106">Coloca valores constantes en celdas o rangos muy rápidamente.</span><span class="sxs-lookup"><span data-stu-id="6efea-106">Puts constant values into cells or ranges very quickly.</span></span> <span data-ttu-id="6efea-107">Para obtener más información, vea "xlSet and Workbooks with Array Formulas" en [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="6efea-107">For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="6efea-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="6efea-108">Parameters</span></span>

<span data-ttu-id="6efea-109">_pxReference_ (**xltypeRef** o **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="6efea-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="6efea-110">Referencia rectangular que describe la celda o celdas de destino.</span><span class="sxs-lookup"><span data-stu-id="6efea-110">A rectangular reference describing the target cell or cells.</span></span> <span data-ttu-id="6efea-111">La referencia debe describir las celdas adyacentes, de modo que en **un xltypeRef** `val.mref.lpmref->count` debe establecerse en 1.</span><span class="sxs-lookup"><span data-stu-id="6efea-111">The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="6efea-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="6efea-112">_pxValue_</span></span>
  
<span data-ttu-id="6efea-113">Valor o valores que se colocarán en la celda o celdas.</span><span class="sxs-lookup"><span data-stu-id="6efea-113">The value or values to be placed into the cell or cells.</span></span> <span data-ttu-id="6efea-114">Si desea más información, vea la sección "Comentarios".</span><span class="sxs-lookup"><span data-stu-id="6efea-114">For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6efea-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6efea-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="6efea-116">argumento pxValue</span><span class="sxs-lookup"><span data-stu-id="6efea-116">pxValue argument</span></span>

<span data-ttu-id="6efea-117">_pxValue_ puede ser un valor o una matriz.</span><span class="sxs-lookup"><span data-stu-id="6efea-117">_pxValue_ can either be a value or an array.</span></span> <span data-ttu-id="6efea-118">Si es un valor, todo el intervalo de destino se rellena con ese valor.</span><span class="sxs-lookup"><span data-stu-id="6efea-118">If it is a value, the entire destination range is filled with that value.</span></span> <span data-ttu-id="6efea-119">Si se trata de una matriz (**xltypeMulti**), los elementos de la matriz se ponen en las ubicaciones correspondientes del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="6efea-119">If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="6efea-120">Si usa una matriz horizontal para el segundo argumento, se duplica hacia abajo para rellenar todo el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="6efea-120">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle.</span></span> <span data-ttu-id="6efea-121">Si usa una matriz vertical, se duplica a la derecha para rellenar todo el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="6efea-121">If you use a vertical array, it is duplicated right to fill the entire rectangle.</span></span> <span data-ttu-id="6efea-122">Si usa una matriz rectangular y es demasiado pequeña para el intervalo rectangular en el que desea colocarla, dicho intervalo se agrega con **#N/A** s.</span><span class="sxs-lookup"><span data-stu-id="6efea-122">If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A** s.</span></span>
  
<span data-ttu-id="6efea-123">Si el intervalo de destino es menor que la matriz de origen, los valores se copian hasta los límites del intervalo de destino y se omiten los datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="6efea-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="6efea-124">Para borrar un elemento del rectángulo de destino, use un elemento de matriz de tipo **xltypeNil** en la matriz de origen.</span><span class="sxs-lookup"><span data-stu-id="6efea-124">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array.</span></span> <span data-ttu-id="6efea-125">Para borrar todo el rectángulo de destino, omita el segundo argumento.</span><span class="sxs-lookup"><span data-stu-id="6efea-125">To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="6efea-126">Restricciones</span><span class="sxs-lookup"><span data-stu-id="6efea-126">Restrictions</span></span>

<span data-ttu-id="6efea-127">**xlSet** no se puede deshacer.</span><span class="sxs-lookup"><span data-stu-id="6efea-127">**xlSet** cannot be undone.</span></span> <span data-ttu-id="6efea-128">Además, destruye cualquier información de deshacer que haya estado disponible antes.</span><span class="sxs-lookup"><span data-stu-id="6efea-128">In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="6efea-129">**xlSet** solo puede colocar constantes, no fórmulas, en celdas.</span><span class="sxs-lookup"><span data-stu-id="6efea-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="6efea-130">**xlSet se** comporta como una función equivalente a un comando de clase 3; es decir, solo está disponible dentro de un ARCHIVO DLL cuando se llama a la  DLL desde un objeto, macro, menú, barra de herramientas, tecla de método  abreviado o el botón Ejecutar del cuadro de diálogo **Macro** (al que se accede desde la pestaña Ver de la cinta de opciones a partir de Excel 2007 y el menú Herramientas en versiones anteriores). </span><span class="sxs-lookup"><span data-stu-id="6efea-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="6efea-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6efea-131">Example</span></span>

<span data-ttu-id="6efea-132">En el siguiente ejemplo se rellena B205:B206 con el valor que se pasó desde una macro.</span><span class="sxs-lookup"><span data-stu-id="6efea-132">The following example fills B205:B206 with the value that was passed in from a macro.</span></span> <span data-ttu-id="6efea-133">Este ejemplo de función de comando requiere un argumento, por lo que solo funcionará si se llama desde una hoja de macros XLM o desde un módulo VBA mediante el **método Application.Run.**</span><span class="sxs-lookup"><span data-stu-id="6efea-133">This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="6efea-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="6efea-134">See also</span></span>

- [<span data-ttu-id="6efea-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="6efea-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="6efea-136">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="6efea-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

