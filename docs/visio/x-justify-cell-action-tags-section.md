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
description: Desplazamiento x del botón de etiqueta de acción en relación con el punto definido por las celdas X e y.
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284975"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="37739-103">Celda X Justify (sección de etiquetas de acción)</span><span class="sxs-lookup"><span data-stu-id="37739-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="37739-104">Desplazamiento *x* del botón de etiqueta de acción en relación con el punto definido por las celdas x e y.</span><span class="sxs-lookup"><span data-stu-id="37739-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="37739-105">En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="37739-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="37739-106">**Value**</span><span class="sxs-lookup"><span data-stu-id="37739-106">**Value**</span></span>|<span data-ttu-id="37739-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37739-107">**Description**</span></span>|<span data-ttu-id="37739-108">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="37739-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="37739-109">comprendi</span><span class="sxs-lookup"><span data-stu-id="37739-109">0</span></span>  <br/> | <span data-ttu-id="37739-110">Justificado a la izquierda (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="37739-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="37739-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="37739-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="37739-112">1</span><span class="sxs-lookup"><span data-stu-id="37739-112">1</span></span>  <br/> | <span data-ttu-id="37739-113">Centrada.</span><span class="sxs-lookup"><span data-stu-id="37739-113">Centered.</span></span>  <br/> |<span data-ttu-id="37739-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="37739-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="37739-115">segundo</span><span class="sxs-lookup"><span data-stu-id="37739-115">2</span></span>  <br/> | <span data-ttu-id="37739-116">Justificado a la derecha.</span><span class="sxs-lookup"><span data-stu-id="37739-116">Right justified.</span></span>  <br/> |<span data-ttu-id="37739-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="37739-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37739-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37739-118">Remarks</span></span>

<span data-ttu-id="37739-119">Las celdas X Justify e y Justify determinan dónde se coloca el botón de etiqueta de acción en relación con el punto definido en las celdas X e y.</span><span class="sxs-lookup"><span data-stu-id="37739-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="37739-120">Para obtener una referencia a la celda X Justify por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="37739-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37739-121">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="37739-121">Cell name:</span></span>  <br/> | <span data-ttu-id="37739-122">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="37739-122">SmartTags.</span></span>  <span data-ttu-id="37739-123">*nombre* . XJustify donde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="37739-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="37739-124">*nombre* es el nombre de la fila de la etiqueta de acción.</span><span class="sxs-lookup"><span data-stu-id="37739-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="37739-125">Para obtener una referencia desde un programa a la celda X Justify por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="37739-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37739-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="37739-126">Section index:</span></span>  <br/> |<span data-ttu-id="37739-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="37739-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="37739-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="37739-128">Row index:</span></span>  <br/> |<span data-ttu-id="37739-129">**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="37739-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="37739-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="37739-130">Cell index:</span></span>  <br/> |<span data-ttu-id="37739-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="37739-131">**visSmartTagXJustify**</span></span> <br/> |
   

