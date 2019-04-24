---
title: Celda PageLeftMargin (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
localization_priority: Normal
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Especifica el margen izquierdo de la página impresa.
ms.openlocfilehash: 289bd0bf16c6dcd9b26ec1a8c7920a29dab724a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334464"
---
# <a name="pageleftmargin-cell-print-properties-section"></a><span data-ttu-id="f6bbd-103">Celda PageLeftMargin (Sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="f6bbd-103">PageLeftMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="f6bbd-104">Especifica el margen izquierdo de la página impresa.</span><span class="sxs-lookup"><span data-stu-id="f6bbd-104">Specifies the margin on the left of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6bbd-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f6bbd-105">Remarks</span></span>

<span data-ttu-id="f6bbd-p101">Este valor representa unidades físicas y no se ve afectado por escalas ni unidades de dibujo. Por ejemplo, si esta celda tiene el valor 0,25 pda., este margen será de 0,25 pulgadas incluso si se utilizan pies como unidades en la página. Si las unidades no se indican explícitamente, este valor asume de forma predeterminada las unidades de la página.</span><span class="sxs-lookup"><span data-stu-id="f6bbd-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.25 in., this margin is 0.25 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="f6bbd-109">Para obtener una referencia a la celda PageLeftMargin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="f6bbd-109">To get a reference to the PageLeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f6bbd-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f6bbd-110">Cell name:</span></span>  <br/> | <span data-ttu-id="f6bbd-111">PageLeftMargin</span><span class="sxs-lookup"><span data-stu-id="f6bbd-111">PageLeftMargin</span></span>  <br/> |
   
<span data-ttu-id="f6bbd-112">Para obtener una referencia desde un programa a la celda PageLeftMargin por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f6bbd-112">To get a reference to the PageLeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f6bbd-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f6bbd-113">Section index:</span></span>  <br/> |<span data-ttu-id="f6bbd-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f6bbd-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f6bbd-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f6bbd-115">Row index:</span></span>  <br/> |<span data-ttu-id="f6bbd-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="f6bbd-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="f6bbd-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f6bbd-117">Cell index:</span></span>  <br/> |<span data-ttu-id="f6bbd-118">**visPrintPropertiesLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="f6bbd-118">**visPrintPropertiesLeftMargin**</span></span> <br/> |
   

