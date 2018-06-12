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
ms.openlocfilehash: ff052c5b254f9b49a97f5d362a4643e16a27b85d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821522"
---
# <a name="angle-cell-shape-transform-section"></a><span data-ttu-id="74112-104">Celda Angle (Sección de transformación de forma)</span><span class="sxs-lookup"><span data-stu-id="74112-104">Angle Cell (Shape Transform Section)</span></span>

<span data-ttu-id="74112-p102">Representa el actual ángulo de giro de la forma en relación con su forma principal. La fórmula predeterminada para determinar el ángulo de giro de una forma 1-D es: =ATAN2(YFin-YInicio,XFin-XInicio).</span><span class="sxs-lookup"><span data-stu-id="74112-p102">Represents the shape's current angle of rotation in relation to its parent. The default formula for determining the rotation angle of a 1-D shape is: =ATAN2(EndY-BeginY,EndX-BeginX).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="74112-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74112-107">Remarks</span></span>

<span data-ttu-id="74112-108">Para obtener una referencia a la celda Angle por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="74112-108">To get a reference to the Angle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74112-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="74112-109">Cell name:</span></span>  <br/> | <span data-ttu-id="74112-110">Angle</span><span class="sxs-lookup"><span data-stu-id="74112-110">Angle</span></span>  <br/> |
   
<span data-ttu-id="74112-111">Para obtener una referencia a la celda Angle por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="74112-111">To get a reference to the Angle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74112-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="74112-112">Section index:</span></span>  <br/> |<span data-ttu-id="74112-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="74112-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="74112-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="74112-114">Row index:</span></span>  <br/> |<span data-ttu-id="74112-115">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="74112-115">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="74112-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="74112-116">Cell index:</span></span>  <br/> |<span data-ttu-id="74112-117">**visXFormAngle**</span><span class="sxs-lookup"><span data-stu-id="74112-117">**visXFormAngle**</span></span> <br/> |
   

