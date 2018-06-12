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
ms.openlocfilehash: 5537cbdcd49c66f3bc28a58051f6e2888a290cd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823430"
---
# <a name="transparency-cell-image-properties-section"></a><span data-ttu-id="69267-103">Celda Transparency (Sección de propiedades de la imagen)</span><span class="sxs-lookup"><span data-stu-id="69267-103">Transparency Cell (Image Properties Section)</span></span>

<span data-ttu-id="69267-104">Determina el grado de transparencia del color de una capa.</span><span class="sxs-lookup"><span data-stu-id="69267-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="69267-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="69267-105">**Value**</span></span>|<span data-ttu-id="69267-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69267-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69267-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="69267-107">0 - 100</span></span>  <br/> |<span data-ttu-id="69267-p101">Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="69267-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69267-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69267-110">Remarks</span></span>

<span data-ttu-id="69267-111">Los valores se redondean al porcentaje medio más próximo.</span><span class="sxs-lookup"><span data-stu-id="69267-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="69267-112">Un valor de 100% es completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="69267-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="69267-113">Aunque una capa que tiene un color completamente transparente el mismo en la página de dibujo aparece como una capa que no tiene ningún color, interactúa con otros objetos en la página de la misma manera como si su transparencia fuera 0%.</span><span class="sxs-lookup"><span data-stu-id="69267-113">Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span> <span data-ttu-id="69267-114">También puede establecer este valor mediante el control deslizante en el cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio** , en el grupo **Edición** , haga clic en **capas**y, a continuación, haga clic en **Propiedades de las capas**).</span><span class="sxs-lookup"><span data-stu-id="69267-114">You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="69267-115">Para obtener una referencia a la celda Transparency por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="69267-115">To get a reference to the Transparency cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69267-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="69267-116">Cell name:</span></span>  <br/> |<span data-ttu-id="69267-117">Transparency</span><span class="sxs-lookup"><span data-stu-id="69267-117">Transparency</span></span>  <br/> |
   
<span data-ttu-id="69267-118">Para obtener una referencia a la celda Transparency por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="69267-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69267-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="69267-119">Section index:</span></span>  <br/> |<span data-ttu-id="69267-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="69267-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="69267-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="69267-121">Row index:</span></span>  <br/> |<span data-ttu-id="69267-122">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="69267-122">**visRowImage**</span></span> <br/> |
|<span data-ttu-id="69267-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="69267-123">Cell index:</span></span>  <br/> |<span data-ttu-id="69267-124">**visImageTransparency**</span><span class="sxs-lookup"><span data-stu-id="69267-124">**visImageTransparency**</span></span> <br/> |
   

