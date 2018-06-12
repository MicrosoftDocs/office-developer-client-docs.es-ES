---
title: Celda TextBkgndTrans (Sección de formato del bloque de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: Determina el nivel de transparencia del color de fondo del bloque de texto de la forma.
ms.openlocfilehash: d9fee430cb2ccd19e8d6069e7561a8fef409a62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823382"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a><span data-ttu-id="db267-103">Celda TextBkgndTrans (Sección de formato del bloque de texto)</span><span class="sxs-lookup"><span data-stu-id="db267-103">TextBkgndTrans Cell (Text Block Format Section)</span></span>

<span data-ttu-id="db267-104">Determina el nivel de transparencia del color de fondo del bloque de texto de la forma.</span><span class="sxs-lookup"><span data-stu-id="db267-104">Determines the transparency level for the background color of the shape's text block.</span></span>
  
|<span data-ttu-id="db267-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="db267-105">**Value**</span></span>|<span data-ttu-id="db267-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="db267-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db267-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="db267-107">0 - 100</span></span>  <br/> |<span data-ttu-id="db267-p101">Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="db267-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db267-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db267-110">Remarks</span></span>

<span data-ttu-id="db267-p102">Los valores se redondean al medio porcentaje más próximo. El valor 100% hace que sea totalmente transparente. Aunque una forma con fondo de texto totalmente transparente y otra sin fondo de texto tienen la misma apariencia en la página de dibujo, la interacción con los demás objetos de la página se producirá como si su transparencia fuera del 0%.</span><span class="sxs-lookup"><span data-stu-id="db267-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape that has a completely transparent text background appears the same on the drawing page as a shape that has no text background, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="db267-114">También puede establecer este valor mediante el control deslizante en la ficha **fuente** del cuadro de diálogo **texto** (en la ficha **Inicio** , haga clic en la flecha de **fuente** ).</span><span class="sxs-lookup"><span data-stu-id="db267-114">You can also set this value using the slider control on the **Font** tab of the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="db267-115">Para obtener una referencia a la celda TextBkgndTrans por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="db267-115">To get a reference to the TextBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db267-116">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="db267-116">Cell name:</span></span>  <br/> |<span data-ttu-id="db267-117">TextBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="db267-117">TextBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="db267-118">Para obtener una referencia a la celda TextBkgndTrans por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="db267-118">To get a reference to the TextBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db267-119">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="db267-119">Section index:</span></span>  <br/> |<span data-ttu-id="db267-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="db267-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="db267-121">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="db267-121">Row index:</span></span>  <br/> |<span data-ttu-id="db267-122">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="db267-122">**visRowText**</span></span> <br/> |
|<span data-ttu-id="db267-123">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="db267-123">Cell index:</span></span>  <br/> |<span data-ttu-id="db267-124">**visTxtBlkBkgndTrans**</span><span class="sxs-lookup"><span data-stu-id="db267-124">**visTxtBlkBkgndTrans**</span></span> <br/> |
   

