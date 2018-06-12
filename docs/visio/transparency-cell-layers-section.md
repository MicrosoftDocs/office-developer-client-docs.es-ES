---
title: Celda Transparency (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: Determina el grado de transparencia del color de una capa.
ms.openlocfilehash: 7c205612436e7731f268e17c851616beebf809dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823436"
---
# <a name="transparency-cell-layers-section"></a><span data-ttu-id="fd24c-103">Celda Transparency (Sección de capas)</span><span class="sxs-lookup"><span data-stu-id="fd24c-103">Transparency Cell (Layers Section)</span></span>

<span data-ttu-id="fd24c-104">Determina el grado de transparencia del color de una capa.</span><span class="sxs-lookup"><span data-stu-id="fd24c-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="fd24c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fd24c-105">**Value**</span></span>|<span data-ttu-id="fd24c-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fd24c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd24c-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="fd24c-107">0 - 100</span></span>  <br/> |<span data-ttu-id="fd24c-p101">Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="fd24c-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd24c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd24c-110">Remarks</span></span>

<span data-ttu-id="fd24c-111">Los valores se redondean al porcentaje medio más próximo.</span><span class="sxs-lookup"><span data-stu-id="fd24c-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="fd24c-112">Un valor de 100% es completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="fd24c-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="fd24c-113">Aunque una capa que tiene un color completamente transparente el mismo en la página de dibujo aparece como una capa que no tiene ningún color, interactúa con otros objetos en la página de la misma manera como si su transparencia fuera 0%.</span><span class="sxs-lookup"><span data-stu-id="fd24c-113">Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span> <span data-ttu-id="fd24c-114">También puede establecer este valor mediante el control deslizante en el cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio** , en el grupo **Edición** , haga clic en **capas**y, a continuación, haga clic en **Propiedades de las capas**).</span><span class="sxs-lookup"><span data-stu-id="fd24c-114">You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="fd24c-115">Para obtener una referencia a la celda Transparency por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="fd24c-115">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd24c-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="fd24c-116">Cell name:</span></span>  <br/> |<span data-ttu-id="fd24c-117">Layers.ColorTrans [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fd24c-117">Layers.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fd24c-118">Para obtener una referencia a la celda Transparency por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="fd24c-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd24c-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="fd24c-119">Section index:</span></span>  <br/> |<span data-ttu-id="fd24c-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="fd24c-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="fd24c-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="fd24c-121">Row index:</span></span>  <br/> |<span data-ttu-id="fd24c-122">**visRowLayer** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fd24c-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="fd24c-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="fd24c-123">Cell index:</span></span>  <br/> |<span data-ttu-id="fd24c-124">**visLayerColorTrans**</span><span class="sxs-lookup"><span data-stu-id="fd24c-124">**visLayerColorTrans**</span></span> <br/> |
   

