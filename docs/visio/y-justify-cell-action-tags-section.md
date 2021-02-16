---
title: Celda Y Justify (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: Desplazamiento Y del botón de etiqueta de acción en relación con el punto definido por las celdas X e Y.
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419985"
---
# <a name="y-justify-cell-action-tags-section"></a><span data-ttu-id="e6007-103">Celda Y Justify (sección de etiquetas de acción)</span><span class="sxs-lookup"><span data-stu-id="e6007-103">Y Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="e6007-104">Desplazamiento  *Y*  del botón de etiqueta de acción en relación con el punto definido por las celdas X e Y.</span><span class="sxs-lookup"><span data-stu-id="e6007-104">The  *y*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e6007-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="e6007-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="e6007-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e6007-106">**Value**</span></span>|<span data-ttu-id="e6007-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e6007-107">**Description**</span></span>|<span data-ttu-id="e6007-108">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="e6007-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e6007-109">0</span><span class="sxs-lookup"><span data-stu-id="e6007-109">0</span></span>  <br/> | <span data-ttu-id="e6007-110">Justificado arriba (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="e6007-110">Top justified (the default).</span></span>  <br/> |<span data-ttu-id="e6007-111">**visSmartTagYJustifyTop**</span><span class="sxs-lookup"><span data-stu-id="e6007-111">**visSmartTagYJustifyTop**</span></span> <br/> |
| <span data-ttu-id="e6007-112">1 </span><span class="sxs-lookup"><span data-stu-id="e6007-112">1</span></span>  <br/> | <span data-ttu-id="e6007-113">Centrada.</span><span class="sxs-lookup"><span data-stu-id="e6007-113">Centered.</span></span>  <br/> |<span data-ttu-id="e6007-114">**visSmartTagYJustifyMiddle**</span><span class="sxs-lookup"><span data-stu-id="e6007-114">**visSmartTagYJustifyMiddle**</span></span> <br/> |
| <span data-ttu-id="e6007-115">2 </span><span class="sxs-lookup"><span data-stu-id="e6007-115">2</span></span>  <br/> | <span data-ttu-id="e6007-116">Justificado abajo.</span><span class="sxs-lookup"><span data-stu-id="e6007-116">Bottom justified.</span></span>  <br/> |<span data-ttu-id="e6007-117">**visSmartTagYJustifyBottom**</span><span class="sxs-lookup"><span data-stu-id="e6007-117">**visSmartTagYJustifyBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6007-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e6007-118">Remarks</span></span>

<span data-ttu-id="e6007-119">Las celdas X Justify e Y Justify determinan dónde se coloca el botón de etiqueta de acción en relación con el punto definido en las celdas X e Y.</span><span class="sxs-lookup"><span data-stu-id="e6007-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span>
  
<span data-ttu-id="e6007-120">Para obtener una referencia a la celda Y Justify por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e6007-120">To get a reference to the Y Justify cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6007-121">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e6007-121">Cell name:</span></span>  <br/> | <span data-ttu-id="e6007-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="e6007-122">SmartTags.</span></span>  <span data-ttu-id="e6007-123">*nombre*  . YJustifique donde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="e6007-123">*name*  .YJustify           where SmartTags.</span></span> <span data-ttu-id="e6007-124">*es*  el nombre de la fila de etiqueta de acción</span><span class="sxs-lookup"><span data-stu-id="e6007-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="e6007-125">Para obtener una referencia desde un programa a la celda Y Justify por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e6007-125">To get a reference to the Y Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e6007-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e6007-126">Section index:</span></span>  <br/> |<span data-ttu-id="e6007-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="e6007-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="e6007-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e6007-128">Row index:</span></span>  <br/> |<span data-ttu-id="e6007-129">**visRowSmartTag**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e6007-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e6007-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e6007-130">Cell index:</span></span>  <br/> |<span data-ttu-id="e6007-131">**visSmartTagYJustify**</span><span class="sxs-lookup"><span data-stu-id="e6007-131">**visSmartTagYJustify**</span></span> <br/> |
   

