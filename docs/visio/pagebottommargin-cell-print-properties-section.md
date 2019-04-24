---
title: Celda PageBottomMargin (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
localization_priority: Normal
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Especifica el margen inferior de la página impresa.
ms.openlocfilehash: f546d89b8761c6c1b7340af69d2b48f16c180767
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334415"
---
# <a name="pagebottommargin-cell-print-properties-section"></a><span data-ttu-id="d2d3c-103">Celda PageBottomMargin (Sección de propiedades de impresión)</span><span class="sxs-lookup"><span data-stu-id="d2d3c-103">PageBottomMargin Cell (Print Properties Section)</span></span>

<span data-ttu-id="d2d3c-104">Especifica el margen inferior de la página impresa.</span><span class="sxs-lookup"><span data-stu-id="d2d3c-104">Specifies the margin at the bottom of the printed page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2d3c-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2d3c-105">Remarks</span></span>

<span data-ttu-id="d2d3c-p101">Este valor representa unidades físicas y no se ve afectado por escalas ni unidades de dibujo. Por ejemplo, si esta celda tiene el valor 0,5 pulgadas, este margen será de 0,5 pulgadas incluso si se utilizan pies como unidades en la página. Si las unidades no se indican explícitamente, este valor asume de forma predeterminada las unidades de la página.</span><span class="sxs-lookup"><span data-stu-id="d2d3c-p101">This value represents physical units and is unaffected by scale or drawing units. For example, if this cell has a value of 0.5 in., this margin is 0.5 inch even if page units are feet. If units are not explicitly stated, this value defaults to page units.</span></span> 
  
<span data-ttu-id="d2d3c-109">Para obtener una referencia a la celda PageBottomMargin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="d2d3c-109">To get a reference to the PageBottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2d3c-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d2d3c-110">Cell name:</span></span>  <br/> | <span data-ttu-id="d2d3c-111">PageBottomMargin</span><span class="sxs-lookup"><span data-stu-id="d2d3c-111">PageBottomMargin</span></span>  <br/> |
   
<span data-ttu-id="d2d3c-112">Para obtener una referencia desde un programa a la celda PageBottomMargin por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2d3c-112">To get a reference to the PageBottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2d3c-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d2d3c-113">Section index:</span></span>  <br/> |<span data-ttu-id="d2d3c-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d2d3c-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d2d3c-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d2d3c-115">Row index:</span></span>  <br/> |<span data-ttu-id="d2d3c-116">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="d2d3c-116">**visRowPrintProperties**</span></span> <br/> |
| <span data-ttu-id="d2d3c-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d2d3c-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d2d3c-118">**visPrintPropertiesBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="d2d3c-118">**visPrintPropertiesBottomMargin**</span></span> <br/> |
   

