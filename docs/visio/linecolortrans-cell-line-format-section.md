---
title: Celda LineColorTrans (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
localization_priority: Normal
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: Determina el grado de transparencia del color de línea de una forma.
ms.openlocfilehash: 555ea15de0279a37bcf67de7374d922b8692ce02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414441"
---
# <a name="linecolortrans-cell-line-format-section"></a><span data-ttu-id="52860-103">Celda LineColorTrans (sección de formato de línea)</span><span class="sxs-lookup"><span data-stu-id="52860-103">LineColorTrans Cell (Line Format Section)</span></span>

<span data-ttu-id="52860-104">Determina el grado de transparencia del color de línea de una forma.</span><span class="sxs-lookup"><span data-stu-id="52860-104">Determines the transparency level of a shape's line color.</span></span>
  
|<span data-ttu-id="52860-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="52860-105">**Value**</span></span>|<span data-ttu-id="52860-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="52860-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52860-107">0 -100</span><span class="sxs-lookup"><span data-stu-id="52860-107">0 - 100</span></span>  <br/> |<span data-ttu-id="52860-p101">Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="52860-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52860-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52860-110">Remarks</span></span>

<span data-ttu-id="52860-p102">Los valores se redondean al porcentaje medio más próximo. El valor 100% hace que sea totalmente transparente. Aunque en la página de dibujo una forma con un color de línea totalmente transparente y otra sin líneas aparecen igual, la interacción con los demás objetos de la página se producirá como si su transparencia fuera del cero por ciento.</span><span class="sxs-lookup"><span data-stu-id="52860-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent line color appears the same as a shape with no lines on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span> 
  
<span data-ttu-id="52860-114">También puede establecer este valor con el control deslizante en el cuadro de diálogo **Línea** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Línea**, seleccione **Grosor** y, a continuación, haga clic en **Más líneas**).</span><span class="sxs-lookup"><span data-stu-id="52860-114">You can also set this value by using the slider control in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="52860-115">Para obtener una referencia a la celda LineColorTrans por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="52860-115">To get a reference to the LineColorTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52860-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="52860-116">Cell name:</span></span>  <br/> |<span data-ttu-id="52860-117">LineColorTrans</span><span class="sxs-lookup"><span data-stu-id="52860-117">LineColorTrans</span></span>  <br/> |
   
<span data-ttu-id="52860-118">Para obtener una referencia desde un programa a la celda LineColorTrans por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="52860-118">To get a reference to the LineColorTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="52860-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="52860-119">Section index:</span></span>  <br/> |<span data-ttu-id="52860-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="52860-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="52860-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="52860-121">Row index:</span></span>  <br/> |<span data-ttu-id="52860-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="52860-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="52860-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="52860-123">Cell index:</span></span>  <br/> |<span data-ttu-id="52860-124">**visLineColorTrans**</span><span class="sxs-lookup"><span data-stu-id="52860-124">**visLineColorTrans**</span></span> <br/> |
   

