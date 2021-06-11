---
title: Celda X Justify (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: El x -offset del botón de etiqueta de acción con relación al punto definido por las celdas X e Y.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414126"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="9e6c5-103">Celda X Justify (sección de etiquetas de acción)</span><span class="sxs-lookup"><span data-stu-id="9e6c5-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="9e6c5-104">El  *x*  -offset del botón de etiqueta de acción con relación al punto definido por las celdas X e Y.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9e6c5-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="9e6c5-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-106">**Value**</span></span>|<span data-ttu-id="9e6c5-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-107">**Description**</span></span>|<span data-ttu-id="9e6c5-108">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9e6c5-109">0</span><span class="sxs-lookup"><span data-stu-id="9e6c5-109">0</span></span>  <br/> | <span data-ttu-id="9e6c5-110">Justificado a la izquierda (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="9e6c5-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="9e6c5-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="9e6c5-112">1</span><span class="sxs-lookup"><span data-stu-id="9e6c5-112">1</span></span>  <br/> | <span data-ttu-id="9e6c5-113">Centrada.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-113">Centered.</span></span>  <br/> |<span data-ttu-id="9e6c5-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="9e6c5-115">2</span><span class="sxs-lookup"><span data-stu-id="9e6c5-115">2</span></span>  <br/> | <span data-ttu-id="9e6c5-116">Justificado a la derecha.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-116">Right justified.</span></span>  <br/> |<span data-ttu-id="9e6c5-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e6c5-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9e6c5-118">Remarks</span></span>

<span data-ttu-id="9e6c5-119">Las celdas X Justify e Y Justify determinan dónde se coloca el botón de etiqueta de acción en relación con el punto definido en las celdas X e Y.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="9e6c5-120">Para obtener una referencia a la celda X Justify por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="9e6c5-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e6c5-121">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9e6c5-121">Cell name:</span></span>  <br/> | <span data-ttu-id="9e6c5-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-122">SmartTags.</span></span>  <span data-ttu-id="9e6c5-123">*nombre*  . XJustify donde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="9e6c5-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="9e6c5-124">*nombre*  es el nombre de la fila de etiqueta de acción</span><span class="sxs-lookup"><span data-stu-id="9e6c5-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="9e6c5-125">Para obtener una referencia desde un programa a la celda X Justify por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9e6c5-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e6c5-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9e6c5-126">Section index:</span></span>  <br/> |<span data-ttu-id="9e6c5-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="9e6c5-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9e6c5-128">Row index:</span></span>  <br/> |<span data-ttu-id="9e6c5-129">**visRowSmartTag**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9e6c5-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9e6c5-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9e6c5-130">Cell index:</span></span>  <br/> |<span data-ttu-id="9e6c5-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="9e6c5-131">**visSmartTagXJustify**</span></span> <br/> |
   

