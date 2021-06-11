---
title: Celda EndArrow (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Indica si una línea tiene una punta de flecha u otro formato de extremo de línea como vértice final. final.
ms.openlocfilehash: 54ef11125a8774914a60897850fb75cd4ab949a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434686"
---
# <a name="endarrow-cell-line-format-section"></a><span data-ttu-id="69bcf-103">Celda EndArrow (Sección de formato de línea)</span><span class="sxs-lookup"><span data-stu-id="69bcf-103">EndArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="69bcf-104">Indica si una línea tiene una punta de flecha u otro formato de extremo de línea como vértice final. final.</span><span class="sxs-lookup"><span data-stu-id="69bcf-104">Indicates whether a line has an arrowhead or other line end format at its last vertex.</span></span>
  
|<span data-ttu-id="69bcf-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="69bcf-105">**Value**</span></span>|<span data-ttu-id="69bcf-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69bcf-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69bcf-107">0</span><span class="sxs-lookup"><span data-stu-id="69bcf-107">0</span></span>  <br/> |<span data-ttu-id="69bcf-108">No hay punta de flecha.</span><span class="sxs-lookup"><span data-stu-id="69bcf-108">No arrowhead.</span></span>  <br/> |
|<span data-ttu-id="69bcf-109">1 -45</span><span class="sxs-lookup"><span data-stu-id="69bcf-109">1 - 45</span></span>  <br/> |<span data-ttu-id="69bcf-110">Varios estilos de punta de flecha que se corresponden con las entradas indizadas del cuadro de diálogo **Línea**.</span><span class="sxs-lookup"><span data-stu-id="69bcf-110">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69bcf-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69bcf-111">Remarks</span></span>

<span data-ttu-id="69bcf-112">También puede establecer este valor en el cuadro de diálogo **Línea** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Línea**, elija **Flechas** y, a continuación, haga clic en **Más flechas**).</span><span class="sxs-lookup"><span data-stu-id="69bcf-112">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span> <span data-ttu-id="69bcf-113">El tamaño de la punta de flecha se establece en la celda EndArrowSize.</span><span class="sxs-lookup"><span data-stu-id="69bcf-113">The size of the arrowhead is set in the EndArrowSize cell.</span></span>
  
<span data-ttu-id="69bcf-114">Puede especificar un extremo de línea personalizada con la función USE en esta celda.</span><span class="sxs-lookup"><span data-stu-id="69bcf-114">You can specify a custom line end using the USE function in this cell.</span></span> 
  
<span data-ttu-id="69bcf-115">Para obtener una referencia a la celda EndArrow por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="69bcf-115">To get a reference to the EndArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69bcf-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="69bcf-116">Cell name:</span></span>  <br/> |<span data-ttu-id="69bcf-117">EndArrow</span><span class="sxs-lookup"><span data-stu-id="69bcf-117">EndArrow</span></span>  <br/> |
   
<span data-ttu-id="69bcf-118">Para obtener una referencia desde un programa a la celda EndArrow por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="69bcf-118">To get a reference to the EndArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69bcf-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="69bcf-119">Section index:</span></span>  <br/> |<span data-ttu-id="69bcf-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="69bcf-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="69bcf-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="69bcf-121">Row index:</span></span>  <br/> |<span data-ttu-id="69bcf-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="69bcf-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="69bcf-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="69bcf-123">Cell index:</span></span>  <br/> |<span data-ttu-id="69bcf-124">**visLineEndArrow**</span><span class="sxs-lookup"><span data-stu-id="69bcf-124">**visLineEndArrow**</span></span> <br/> |
   

