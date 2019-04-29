---
title: Celda Glue (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Determina si las formas que pertenecen a la capa pueden pegarse.
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408519"
---
# <a name="glue-cell-layers-section"></a><span data-ttu-id="be8b5-103">Celda Glue (Sección de capas)</span><span class="sxs-lookup"><span data-stu-id="be8b5-103">Glue Cell (Layers Section)</span></span>

<span data-ttu-id="be8b5-104">Determina si las formas que pertenecen a la capa pueden pegarse.</span><span class="sxs-lookup"><span data-stu-id="be8b5-104">Specifies whether shapes belonging to the layer can be glued.</span></span>
  
|<span data-ttu-id="be8b5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="be8b5-105">**Value**</span></span>|<span data-ttu-id="be8b5-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="be8b5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="be8b5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="be8b5-107">TRUE</span></span>  <br/> |<span data-ttu-id="be8b5-108">Se pueden pegar.</span><span class="sxs-lookup"><span data-stu-id="be8b5-108">Glue is enabled.</span></span>  <br/> |
|<span data-ttu-id="be8b5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="be8b5-109">FALSE</span></span>  <br/> |<span data-ttu-id="be8b5-110">No se pueden pegar.</span><span class="sxs-lookup"><span data-stu-id="be8b5-110">Glue is disabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be8b5-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be8b5-111">Remarks</span></span>

<span data-ttu-id="be8b5-112">Esta celda corresponde a la **opción Pegar** del cuadro de diálogo Propiedades de las **capas** (en la ficha **Inicio** , en el grupo **edición** , haga clic en **capas**y, a continuación, en **propiedades de las capas** ).</span><span class="sxs-lookup"><span data-stu-id="be8b5-112">This cell corresponds to the **Glue** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="be8b5-113">Para obtener una referencia a la celda Glue por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="be8b5-113">To get a reference to the Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be8b5-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="be8b5-114">Cell name:</span></span>  <br/> |<span data-ttu-id="be8b5-115">Layers. Glue [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="be8b5-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="be8b5-116">Para obtener una referencia desde un programa a la celda Glue por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="be8b5-116">To get a reference to the Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be8b5-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="be8b5-117">Section index:</span></span>  <br/> |<span data-ttu-id="be8b5-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="be8b5-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="be8b5-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="be8b5-119">Row index:</span></span>  <br/> |<span data-ttu-id="be8b5-120">**visRowLayer** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="be8b5-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="be8b5-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="be8b5-121">Cell index:</span></span>  <br/> |<span data-ttu-id="be8b5-122">**visLayerGlue**</span><span class="sxs-lookup"><span data-stu-id="be8b5-122">**visLayerGlue**</span></span> <br/> |
   

