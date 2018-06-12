---
title: Celda Width (Sección de transformación de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 'Contiene el ancho de la forma seleccionada en las unidades especificadas para el dibujo. La fórmula predeterminada para especificar el ancho de una forma 1D es:'
ms.openlocfilehash: 55e77c5ccfca2425a8a2985564448e0f656aebbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823540"
---
# <a name="width-cell-shape-transform-section"></a><span data-ttu-id="20d3d-104">Celda Width (Sección de transformación de forma)</span><span class="sxs-lookup"><span data-stu-id="20d3d-104">Width Cell (Shape Transform Section)</span></span>

<span data-ttu-id="20d3d-p102">Contiene el ancho de la forma seleccionada en las unidades especificadas para el dibujo. La fórmula predeterminada para especificar el ancho de una forma 1D es:</span><span class="sxs-lookup"><span data-stu-id="20d3d-p102">Contains the width of the selected shape in drawing units. The default formula for determining the width of a 1-D shape is:</span></span>
  
<span data-ttu-id="20d3d-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="20d3d-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20d3d-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20d3d-108">Remarks</span></span>

<span data-ttu-id="20d3d-109">Para obtener una referencia a la celda Width por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="20d3d-109">To get a reference to the Width cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20d3d-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="20d3d-110">Cell name:</span></span>  <br/> | <span data-ttu-id="20d3d-111">Width</span><span class="sxs-lookup"><span data-stu-id="20d3d-111">Width</span></span>  <br/> |
   
<span data-ttu-id="20d3d-112">Para obtener una referencia a la celda Width por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="20d3d-112">To get a reference to the Width cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20d3d-113">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="20d3d-113">Section index:</span></span>  <br/> |<span data-ttu-id="20d3d-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="20d3d-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="20d3d-115">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="20d3d-115">Row index:</span></span>  <br/> |<span data-ttu-id="20d3d-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="20d3d-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="20d3d-117">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="20d3d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="20d3d-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="20d3d-118">**visXFormWidth**</span></span> <br/> |
   

