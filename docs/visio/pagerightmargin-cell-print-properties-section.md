---
title: Celda PageRightMargin (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: Especifica el margen derecho de la página impresa.
ms.openlocfilehash: d30669626fe07379521d61554010ae1bd7b0e83a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339497"
---
# <a name="pagerightmargin-cell-print-properties-section"></a><span data-ttu-id="42e54-103">Celda PageRightMargin (Sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="42e54-103">PageRightMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="42e54-104">Especifica el margen derecho de la página impresa.</span><span class="sxs-lookup"><span data-stu-id="42e54-104">Specifies the margin on the right of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42e54-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42e54-105">Remarks</span></span>

<span data-ttu-id="42e54-p101">Este valor representa unidades físicas y no se ve afectado por escalas ni unidades de dibujo. Por ejemplo, si esta celda tiene el valor 0,25 pda., este margen será de 0,25 pulgadas incluso si se utilizan pies como unidades en la página. Si las unidades no se indican explícitamente, este valor asume de forma predeterminada las unidades de la página.</span><span class="sxs-lookup"><span data-stu-id="42e54-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="42e54-109">Para obtener una referencia a la celda PageRightMargin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="42e54-109">To get a reference to the PageRightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="42e54-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="42e54-110">Cell name:</span></span>  <br/> | <span data-ttu-id="42e54-111">PageRightMargin</span><span class="sxs-lookup"><span data-stu-id="42e54-111">PageRightMargin</span></span>  <br/> |
   
<span data-ttu-id="42e54-112">Para obtener una referencia desde un programa a la celda PageRightMargin por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="42e54-112">To get a reference to the PageRightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="42e54-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="42e54-113">Section index:</span></span>  <br/> |<span data-ttu-id="42e54-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="42e54-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="42e54-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="42e54-115">Row index:</span></span>  <br/> |<span data-ttu-id="42e54-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="42e54-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="42e54-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="42e54-117">Cell index:</span></span>  <br/> |<span data-ttu-id="42e54-118">**visPrintPropertiesRightMargin**</span><span class="sxs-lookup"><span data-stu-id="42e54-118">**visPrintPropertiesRightMargin**</span></span> <br/> |
   

