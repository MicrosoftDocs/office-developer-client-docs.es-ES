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
ms.openlocfilehash: fe0aacf167b2400ca10e22a70c9086429f6059f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436380"
---
# <a name="transparency-cell-layers-section"></a><span data-ttu-id="06f9f-103">Celda Transparency (Sección de capas)</span><span class="sxs-lookup"><span data-stu-id="06f9f-103">Transparency Cell (Layers Section)</span></span>

<span data-ttu-id="06f9f-104">Determina el grado de transparencia del color de una capa.</span><span class="sxs-lookup"><span data-stu-id="06f9f-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="06f9f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="06f9f-105">**Value**</span></span>|<span data-ttu-id="06f9f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06f9f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06f9f-107">0 -100</span><span class="sxs-lookup"><span data-stu-id="06f9f-107">0 - 100</span></span>  <br/> |<span data-ttu-id="06f9f-p101">Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="06f9f-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06f9f-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06f9f-110">Remarks</span></span>

<span data-ttu-id="06f9f-p102">Los valores se redondean al medio porcentaje más próximo. El valor 100% es totalmente transparente. Aunque una capa con un color totalmente transparente y otra sin color tienen la misma apariencia en la página de dibujo, la interacción con los demás objetos de la página es la misma que si su transparencia fuera del 0%. Para establecer este valor, también puede usar el control deslizante del cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).</span><span class="sxs-lookup"><span data-stu-id="06f9f-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%. You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="06f9f-115">Para obtener una referencia a la celda Transparency por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="06f9f-115">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06f9f-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="06f9f-116">Cell name:</span></span>  <br/> |<span data-ttu-id="06f9f-117">Layers.ColorTrans[ *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="06f9f-117">Layers.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="06f9f-118">Para obtener una referencia desde un programa a la celda Transparency por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="06f9f-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06f9f-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="06f9f-119">Section index:</span></span>  <br/> |<span data-ttu-id="06f9f-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="06f9f-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="06f9f-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="06f9f-121">Row index:</span></span>  <br/> |<span data-ttu-id="06f9f-122">**visRowLayer**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="06f9f-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="06f9f-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="06f9f-123">Cell index:</span></span>  <br/> |<span data-ttu-id="06f9f-124">**visLayerColorTrans**</span><span class="sxs-lookup"><span data-stu-id="06f9f-124">**visLayerColorTrans**</span></span> <br/> |
   

