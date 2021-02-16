---
title: Celda Transparency (Sección de propiedades de la imagen)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: Determina el grado de transparencia del color de una capa.
ms.openlocfilehash: defe5307e57c433fcf85a4132939d08cb1ddec77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405838"
---
# <a name="transparency-cell-image-properties-section"></a><span data-ttu-id="5bc0f-103">Celda Transparency (sección de propiedades de la imagen)</span><span class="sxs-lookup"><span data-stu-id="5bc0f-103">Transparency Cell (Image Properties Section)</span></span>

<span data-ttu-id="5bc0f-104">Determina el grado de transparencia del color de una capa.</span><span class="sxs-lookup"><span data-stu-id="5bc0f-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="5bc0f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5bc0f-105">**Value**</span></span>|<span data-ttu-id="5bc0f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5bc0f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5bc0f-107">0 -100</span><span class="sxs-lookup"><span data-stu-id="5bc0f-107">0 - 100</span></span>  <br/> |<span data-ttu-id="5bc0f-p101">Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="5bc0f-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bc0f-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5bc0f-110">Remarks</span></span>

<span data-ttu-id="5bc0f-p102">Los valores se redondean al medio porcentaje más próximo. El valor 100% es totalmente transparente. Aunque una capa con un color totalmente transparente y otra sin color tienen la misma apariencia en la página de dibujo, la interacción con los demás objetos de la página es la misma que si su transparencia fuera del 0%. Para establecer este valor, también puede usar el control deslizante del cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).</span><span class="sxs-lookup"><span data-stu-id="5bc0f-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%. You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="5bc0f-115">Para obtener una referencia a la celda Transparency por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="5bc0f-115">To get a reference to the Transparency cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bc0f-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5bc0f-116">Cell name:</span></span>  <br/> |<span data-ttu-id="5bc0f-117">Transparencia</span><span class="sxs-lookup"><span data-stu-id="5bc0f-117">Transparency</span></span>  <br/> |
   
<span data-ttu-id="5bc0f-118">Para obtener una referencia desde un programa a la celda Transparency por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5bc0f-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bc0f-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5bc0f-119">Section index:</span></span>  <br/> |<span data-ttu-id="5bc0f-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5bc0f-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5bc0f-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5bc0f-121">Row index:</span></span>  <br/> |<span data-ttu-id="5bc0f-122">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="5bc0f-122">**visRowImage**</span></span> <br/> |
|<span data-ttu-id="5bc0f-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5bc0f-123">Cell index:</span></span>  <br/> |<span data-ttu-id="5bc0f-124">**visImageTransparency**</span><span class="sxs-lookup"><span data-stu-id="5bc0f-124">**visImageTransparency**</span></span> <br/> |
   

