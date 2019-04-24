---
title: Celda Snap (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
localization_priority: Normal
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: Determina si otras formas se pueden ajustar a formas asignadas a la capa. Las formas asignadas a la capa pueden ajustarse a otras formas, pero no a la inversa.
ms.openlocfilehash: 87e7e7500469fb7f8c7fdd4771a0225d0e4fc993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359811"
---
# <a name="snap-cell-layers-section"></a><span data-ttu-id="b80b9-104">Celda Snap (Sección de capas)</span><span class="sxs-lookup"><span data-stu-id="b80b9-104">Snap Cell (Layers Section)</span></span>

<span data-ttu-id="b80b9-p102">Determina si otras formas se pueden ajustar a formas asignadas a la capa. Las formas asignadas a la capa pueden ajustarse a otras formas, pero no a la inversa.</span><span class="sxs-lookup"><span data-stu-id="b80b9-p102">Determines whether other shapes can snap to shapes assigned to the layer. Shapes assigned to the layer can snap to other shapes, but other shapes can't snap to them.</span></span>
  
|<span data-ttu-id="b80b9-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="b80b9-107">**Value**</span></span>|<span data-ttu-id="b80b9-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b80b9-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b80b9-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="b80b9-109">TRUE</span></span>  <br/> |<span data-ttu-id="b80b9-110">Las demás formas pueden ajustarse a las formas de la capa.</span><span class="sxs-lookup"><span data-stu-id="b80b9-110">Other shapes can snap to shapes on the layer.</span></span>  <br/> |
|<span data-ttu-id="b80b9-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="b80b9-111">FALSE</span></span>  <br/> |<span data-ttu-id="b80b9-112">Las demás formas no pueden ajustarse a las formas de la capa.</span><span class="sxs-lookup"><span data-stu-id="b80b9-112">Other shapes cannot snap to shapes on the layer.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b80b9-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b80b9-113">Remarks</span></span>

<span data-ttu-id="b80b9-114">También puede usar la opción **Ajustar** en el cuadro de diálogo **Propiedades de las capas** para establecer este valor (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).</span><span class="sxs-lookup"><span data-stu-id="b80b9-114">You can also set the value of this cell using the **Snap** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="b80b9-115">Para obtener una referencia a la celda Snap por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="b80b9-115">To get a reference to the Snap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b80b9-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b80b9-116">Cell name:</span></span>  <br/> |<span data-ttu-id="b80b9-117">Layers. Snap [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b80b9-117">Layers.Snap[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b80b9-118">Para obtener una referencia desde un programa a la celda Snap por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b80b9-118">To get a reference to the Snap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b80b9-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b80b9-119">Section index:</span></span>  <br/> |<span data-ttu-id="b80b9-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="b80b9-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="b80b9-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b80b9-121">Row index:</span></span>  <br/> |<span data-ttu-id="b80b9-122">**visRowLayer** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b80b9-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b80b9-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b80b9-123">Cell index:</span></span>  <br/> |<span data-ttu-id="b80b9-124">**visLayerSnap**</span><span class="sxs-lookup"><span data-stu-id="b80b9-124">**visLayerSnap**</span></span> <br/> |
   

