---
title: Celda Visible (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Especifica si las formas de la capa son visibles en la página de dibujo.
ms.openlocfilehash: 9a025403b1f5b46d2f439805a15954eaeeab2686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823517"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="c2020-103">Celda Visible (sección Capas)</span><span class="sxs-lookup"><span data-stu-id="c2020-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="c2020-104">Especifica si las formas de la capa son visibles en la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="c2020-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="c2020-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c2020-105">**Value**</span></span>|<span data-ttu-id="c2020-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2020-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2020-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c2020-107">TRUE</span></span>  <br/> |<span data-ttu-id="c2020-108">Las formas son visibles.</span><span class="sxs-lookup"><span data-stu-id="c2020-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="c2020-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c2020-109">FALSE</span></span>  <br/> |<span data-ttu-id="c2020-110">Las formas están ocultas.</span><span class="sxs-lookup"><span data-stu-id="c2020-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2020-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2020-111">Remarks</span></span>

<span data-ttu-id="c2020-112">Esta celda corresponde a la opción **Visible** en el cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio** , en el grupo **Edición** , haga clic en **capas**y, a continuación, haga clic en **Propiedades de las capas** ).</span><span class="sxs-lookup"><span data-stu-id="c2020-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="c2020-113">Para obtener una referencia a la celda Visible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="c2020-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2020-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c2020-114">Cell name:</span></span>  <br/> |<span data-ttu-id="c2020-115">Layers.Visible [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c2020-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c2020-116">Para obtener una referencia desde un programa a la celda Visible por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c2020-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2020-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c2020-117">Section index:</span></span>  <br/> |<span data-ttu-id="c2020-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="c2020-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="c2020-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c2020-119">Row index:</span></span>  <br/> |<span data-ttu-id="c2020-120">**visRowLayer** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c2020-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c2020-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c2020-121">Cell index:</span></span>  <br/> |<span data-ttu-id="c2020-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="c2020-122">**visLayerVisible**</span></span> <br/> |
   

