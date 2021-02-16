---
title: Celda Angle (Sección de transformación de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 'Representa el actual ángulo de giro de la forma en relación con su forma principal. La fórmula predeterminada para determinar el ángulo de giro de una forma 1-D es: =ATAN2(YFin-YInicio,XFin-XInicio).'
ms.openlocfilehash: 85f64c6111b492940d278a5558508a2dea6b1e1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414553"
---
# <a name="angle-cell-shape-transform-section"></a><span data-ttu-id="3b6ae-104">Celda Angle (Sección de transformación de forma)</span><span class="sxs-lookup"><span data-stu-id="3b6ae-104">Angle Cell (Shape Transform Section)</span></span>

<span data-ttu-id="3b6ae-p102">Representa el actual ángulo de giro de la forma en relación con su forma principal. La fórmula predeterminada para determinar el ángulo de giro de una forma 1-D es: =ATAN2(YFin-YInicio,XFin-XInicio).</span><span class="sxs-lookup"><span data-stu-id="3b6ae-p102">Represents the shape's current angle of rotation in relation to its parent. The default formula for determining the rotation angle of a 1-D shape is: =ATAN2(EndY-BeginY,EndX-BeginX).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b6ae-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b6ae-107">Remarks</span></span>

<span data-ttu-id="3b6ae-108">Para obtener una referencia a la celda Angle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="3b6ae-108">To get a reference to the Angle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b6ae-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3b6ae-109">Cell name:</span></span>  <br/> | <span data-ttu-id="3b6ae-110">Ángulo</span><span class="sxs-lookup"><span data-stu-id="3b6ae-110">Angle</span></span>  <br/> |
   
<span data-ttu-id="3b6ae-111">Para obtener una referencia a la celda Angle por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3b6ae-111">To get a reference to the Angle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b6ae-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3b6ae-112">Section index:</span></span>  <br/> |<span data-ttu-id="3b6ae-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3b6ae-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3b6ae-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3b6ae-114">Row index:</span></span>  <br/> |<span data-ttu-id="3b6ae-115">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="3b6ae-115">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="3b6ae-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3b6ae-116">Cell index:</span></span>  <br/> |<span data-ttu-id="3b6ae-117">**visXFormAngle**</span><span class="sxs-lookup"><span data-stu-id="3b6ae-117">**visXFormAngle**</span></span> <br/> |
   

