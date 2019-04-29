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
ms.openlocfilehash: 4266debc318c839bdd29fa818d11b5e1da669a9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405453"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="e8bbc-103">Celda Visible (sección de capas)</span><span class="sxs-lookup"><span data-stu-id="e8bbc-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="e8bbc-104">Especifica si las formas de la capa son visibles en la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="e8bbc-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="e8bbc-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e8bbc-105">**Value**</span></span>|<span data-ttu-id="e8bbc-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8bbc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8bbc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e8bbc-107">TRUE</span></span>  <br/> |<span data-ttu-id="e8bbc-108">Las formas son visibles.</span><span class="sxs-lookup"><span data-stu-id="e8bbc-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="e8bbc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e8bbc-109">FALSE</span></span>  <br/> |<span data-ttu-id="e8bbc-110">Las formas están ocultas.</span><span class="sxs-lookup"><span data-stu-id="e8bbc-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8bbc-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8bbc-111">Remarks</span></span>

<span data-ttu-id="e8bbc-112">Esta celda corresponde a la opción **visible** del cuadro de diálogo **propiedades** de las capas (en la ficha **Inicio** , en el grupo **edición** , haga clic en **capas**y, a continuación, en propiedades de las **capas** ).</span><span class="sxs-lookup"><span data-stu-id="e8bbc-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="e8bbc-113">Para obtener una referencia a la celda Visible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="e8bbc-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8bbc-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="e8bbc-114">Cell name:</span></span>  <br/> |<span data-ttu-id="e8bbc-115">Layers. visible [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e8bbc-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e8bbc-116">Para obtener una referencia desde un programa a la celda Visible por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8bbc-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8bbc-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="e8bbc-117">Section index:</span></span>  <br/> |<span data-ttu-id="e8bbc-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="e8bbc-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="e8bbc-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="e8bbc-119">Row index:</span></span>  <br/> |<span data-ttu-id="e8bbc-120">**visRowLayer** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e8bbc-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e8bbc-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="e8bbc-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e8bbc-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="e8bbc-122">**visLayerVisible**</span></span> <br/> |
   

