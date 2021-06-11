---
title: Celda Position (Sección de tabulaciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Especifica la posición de una tabulación. La posición de tabulación no depende de la escala del dibujo. Si se cambia la escala, la posición de tabulación permanece igual.
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409933"
---
# <a name="position-cell-tabs-section"></a><span data-ttu-id="4114e-105">Celda Position (Sección de tabulaciones)</span><span class="sxs-lookup"><span data-stu-id="4114e-105">Position Cell (Tabs Section)</span></span>

<span data-ttu-id="4114e-p102">Especifica la posición de una tabulación. La posición de tabulación no depende de la escala del dibujo. Si se cambia la escala, la posición de tabulación permanece igual.</span><span class="sxs-lookup"><span data-stu-id="4114e-p102">Specifies the position of a tab stop. The tab position is independent of the scale of the drawing. If the drawing is scaled, the tab position remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4114e-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4114e-109">Remarks</span></span>

<span data-ttu-id="4114e-110">Para obtener una referencia a la celda Position por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="4114e-110">To get a reference to the Position cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4114e-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4114e-111">Cell name:</span></span>  <br/> | <span data-ttu-id="4114e-112">Pestañas.</span><span class="sxs-lookup"><span data-stu-id="4114e-112">Tabs.</span></span>  <span data-ttu-id="4114e-113">*ij*            donde  *i*  y  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4114e-113">*ij*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4114e-114">Para obtener una referencia desde un programa a la celda Position por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4114e-114">To get a reference to the Position cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4114e-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4114e-115">Section index:</span></span>  <br/> |<span data-ttu-id="4114e-116">**visSectionTab**</span><span class="sxs-lookup"><span data-stu-id="4114e-116">**visSectionTab**</span></span> <br/> |
| <span data-ttu-id="4114e-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4114e-117">Row index:</span></span>  <br/> |<span data-ttu-id="4114e-118">**visRowTab**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4114e-118">**visRowTab** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4114e-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4114e-119">Cell index:</span></span>  <br/> | <span data-ttu-id="4114e-120">(*j*  \*3) + **visTabPos**</span><span class="sxs-lookup"><span data-stu-id="4114e-120">(*j*  \*3) + **visTabPos**</span></span> <br/> |
   

