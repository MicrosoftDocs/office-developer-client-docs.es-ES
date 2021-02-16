---
title: Referencias hoja de cálculo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- references [excel 2007], worksheet,worksheet references [Excel 2007],external worksheet references [Excel 2007],active worksheet [Excel 2007],current worksheet [Excel 2007],internal worksheet references [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2944f73a3144837a4be8aff7c7fed9a8d2158203
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416464"
---
# <a name="worksheet-references"></a><span data-ttu-id="9ab87-104">Referencias de hojas de cálculo</span><span class="sxs-lookup"><span data-stu-id="9ab87-104">Worksheet References</span></span>

 <span data-ttu-id="9ab87-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9ab87-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9ab87-p101">Una referencia en Microsoft Excel es un tipo de datos que hace referencia a un bloque rectangular de celdas (que pueden ser una sola celda) o, en algunos casos, un número de bloques de celdas no contiguas. Internamente, Excel usa un tipo de referencia para las celdas de la hoja actual, conocido como una referencia interna. Cualquier celda que no se encuentre en la hoja actual se describe con otro tipo de referencia conocida como referencia externa. Consulte la siguiente sección para obtener la definición del activo y el actual.</span><span class="sxs-lookup"><span data-stu-id="9ab87-p101">A reference in Microsoft Excel is a data type that refers to a rectangular block of cells (which can be just one cell), or in some cases, a number of disjoint blocks of cells. Internally, Excel uses one reference type for cells on the current sheet, known as an internal reference. Any cell that is not on the current sheet is described by another type of reference known as an external reference. See the next section for the definition of active and current.</span></span>
  
## <a name="active-vs-current"></a><span data-ttu-id="9ab87-110">Activo y actual</span><span class="sxs-lookup"><span data-stu-id="9ab87-110">Active vs. Current</span></span>

<span data-ttu-id="9ab87-p102">En Excel, el término activo hace referencia a lo que el usuario ve. La hoja de cálculo y el libro activos son los que el usuario está viendo o, si Excel ha perdido el foco en otra aplicación, lo que estaban viendo cuando Excel tenía el último foco. La hoja activa se encuentra siempre en el libro activo. La celda o celdas seleccionadas en la hoja activa se conocen como celdas activas. Si un objeto integrado tiene el foco, las últimas celdas seleccionadas seguirán siendo activas.</span><span class="sxs-lookup"><span data-stu-id="9ab87-p102">In Excel, the term active refers to what the user is viewing. The active workbook and worksheet are those that the user is currently looking at, or, if Excel has lost focus to another application, was looking at when Excel last had focus. The active sheet is always in the active workbook. The one or more cells that are selected in the active sheet are known as the active cells. If an embedded object has focus, the last-selected cells are still active.</span></span> 
  
<span data-ttu-id="9ab87-p103">El término actual hace referencia a lo que Excel recalcula. El libro y la hoja de cálculo actuales son los que actualmente se recalculan. La hoja actual siempre se encuentra en el libro actual. La celda que se recalcula se conoce como la celda actual o, en el caso de una fórmula de matriz que se recalcula, las celdas actuales.</span><span class="sxs-lookup"><span data-stu-id="9ab87-p103">The term current refers to what Excel is recalculating. The current workbook and worksheet are those that are currently being recalculated. The current sheet is always in the current workbook. The cell being recalculated is known as the current cell, or, in the case of an array formula being recalculated, the current cells.</span></span> 
  
<span data-ttu-id="9ab87-120">Los puntos importantes a recordar son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9ab87-120">The important points to remember are as follows:</span></span>
  
- <span data-ttu-id="9ab87-121">Normalmente, el libro, la hoja de cálculo o la celda activos no son los actuales, aunque pueden serlo.</span><span class="sxs-lookup"><span data-stu-id="9ab87-121">The active workbook/worksheet/cell is not generally the current one, although it can be.</span></span>
    
- <span data-ttu-id="9ab87-122">Una función de complemento, ya sea en un módulo de Visual Basic para aplicaciones (VBA), o un DLL o XLL, siempre se llama desde la celda actual en la hoja actual, o uno de ellos en el caso de la actualización multiproceso (MTR).</span><span class="sxs-lookup"><span data-stu-id="9ab87-122">An add-in function, whether in a Visual Basic for Applications (VBA) module or a DLL or XLL, is always called from the current cell on the current sheet, or one of them in the case of multithreaded recalculation (MTR).</span></span>
    
<span data-ttu-id="9ab87-p104">Muchas funciones de Excel que proporcionan información sobre una celda, un rango de celdas o una hoja de un libro, distinguen entre el libro, la hoja o la celda activos, y el libro, la hoja o la celda actuales. Esta diferencia se refleja en los tipos de datos que se usan para describir las referencias a bloques de celdas, como se describe en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="9ab87-p104">Many Excel functions that provide information about a cell, a range of cells, or a sheet in a workbook distinguish between the active workbook, sheet, or cell and the current workbook, sheet, or cell. This difference is reflected in the data types used to describe references to blocks of cells, as described in the following section.</span></span>
  
## <a name="internal-and-external-worksheet-references"></a><span data-ttu-id="9ab87-125">Referencias de hoja de cálculo internas y externas</span><span class="sxs-lookup"><span data-stu-id="9ab87-125">Internal and External Worksheet References</span></span>

<span data-ttu-id="9ab87-p105">La diferencia principal entre las referencias internas y externas es que el tipo de datos de referencia externa contiene un identificador para la hoja de cálculo y también una descripción de las celdas a las que hace referencia. Una referencia interna no contiene ninguna referencia a la hoja, es implícito que la hoja es la hoja actual.</span><span class="sxs-lookup"><span data-stu-id="9ab87-p105">The key difference between internal and external references is that the external reference data type contains an ID for the worksheet and also a description of which cells are referred to. An internal reference contains no reference to the sheet—it is implicit that the sheet is the current sheet.</span></span> 
  
<span data-ttu-id="9ab87-p106">Muchas funciones de la API de C devuelven referencias o toman argumentos de referencia. Cualquier función de la API de C que toma argumentos de referencia acepta referencias externas o internas, excepto la función **xlSheetNm**, que necesita una referencia externa. Algunas funciones solo devuelven referencias internas o externas. Por ejemplo, la función de la API de C [xlfCaller](xlfcaller.md) devuelve una referencia a las celdas de la llamada, por definición, en la hoja actual. La referencia devuelta es siempre una referencia interna, aunque la función puede devolver tipos de no referencia donde no se llama a la función desde una celda de la hoja de cálculo. La función de la API de C [xlSheetId](xlsheetid.md) siempre devuelve el identificador de una hoja de cálculo dentro de un tipo de datos de referencia externa.</span><span class="sxs-lookup"><span data-stu-id="9ab87-p106">Many C API functions return references or take reference arguments. Any C API function that takes reference arguments accepts either internal or external references, except the **xlSheetNm** function, which requires an external reference. Some functions only return either internal or external references. For example, the C API function [xlfCaller](xlfcaller.md) returns a reference to the calling cells, by definition, on the current sheet. The returned reference is always an internal reference, although the function can return non-reference types where the function is not called from a worksheet cell. The C API function [xlSheetId](xlsheetid.md) always returns the ID of a worksheet contained within an external reference data type.</span></span> 
  
<span data-ttu-id="9ab87-p107">La otra diferencia clave entre los tipos de referencia internos y externos es que el tipo de datos de referencia externa puede describir bloques de celdas no contiguos en la misma hoja. Las referencias internas solo pueden describir un único bloque en la hoja actual. Las referencias no contiguas se pueden pasar a cualquier función que tome un argumento de rango.</span><span class="sxs-lookup"><span data-stu-id="9ab87-p107">The other key difference between the internal and external reference types is that the external reference data type can describe multiple disjoint blocks of cells on the same sheet. Internal references can describe only a single block on the current sheet. Disjoint references can be passed to any function that takes a range argument.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ab87-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ab87-137">See also</span></span>



[<span data-ttu-id="9ab87-138">Conceptos de programación de Excel</span><span class="sxs-lookup"><span data-stu-id="9ab87-138">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="9ab87-139">Evaluar los nombres y otras expresiones de fórmulas de la hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="9ab87-139">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[<span data-ttu-id="9ab87-140">Evaluación de expresiones y hojas de cálculo de Excel</span><span class="sxs-lookup"><span data-stu-id="9ab87-140">Excel Worksheet and Expression Evaluation</span></span>](excel-worksheet-and-expression-evaluation.md)

