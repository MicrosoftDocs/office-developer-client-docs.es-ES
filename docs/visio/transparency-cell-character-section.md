---
title: Celda Transparency (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Determina el nivel de transparencia de color de un intervalo de texto de una forma.
ms.openlocfilehash: 8619ec25372ae163fff1759aca36ff6693820e39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280986"
---
# <a name="transparency-cell-character-section"></a><span data-ttu-id="d0887-103">Celda Transparency (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="d0887-103">Transparency Cell (Character Section)</span></span>

<span data-ttu-id="d0887-104">Determina el nivel de transparencia de color de un intervalo de texto de una forma.</span><span class="sxs-lookup"><span data-stu-id="d0887-104">Determines the transparency level for a range of a shape's text color.</span></span>
  
|<span data-ttu-id="d0887-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="d0887-105">**Value**</span></span>|<span data-ttu-id="d0887-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0887-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d0887-107">0 -100</span><span class="sxs-lookup"><span data-stu-id="d0887-107">0 - 100</span></span>  <br/> |<span data-ttu-id="d0887-p101">Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="d0887-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0887-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0887-110">Remarks</span></span>

<span data-ttu-id="d0887-p102">Los valores se redondean al medio porcentaje más próximo. El valor 100% hace que sea totalmente transparente. Aunque una forma con texto totalmente transparente y otra sin texto tienen la misma apariencia en la página de dibujo, la interacción con los demás objetos de la página se producirá como si su transparencia fuera del 0%.</span><span class="sxs-lookup"><span data-stu-id="d0887-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape that has completely transparent text appears the same on the drawing page as a shape that has no text, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="d0887-114">Para establecer este valor, también puede usar el control deslizante en la ficha **fuente** del cuadro de diálogo **texto** (en la ficha **Inicio** , haga clic en la flecha de **fuente** ).</span><span class="sxs-lookup"><span data-stu-id="d0887-114">You can also set this value by using the slider control on the **Font** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="d0887-p103">Si la sección de caracteres contiene varias filas, la celda Transparency contiene la información de formato que se aplica a un subintervalo del texto de la forma. En caso contrario, contiene información de formato para todo el texto de la forma.</span><span class="sxs-lookup"><span data-stu-id="d0887-p103">If the Characters section contains multiple rows, the Transparency cell contains formatting information applied to a sub-range of a shape's text. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="d0887-117">Para obtener una referencia a la celda Transparency por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="d0887-117">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0887-118">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d0887-118">Cell name:</span></span>  <br/> |<span data-ttu-id="d0887-119">Char. ColorTrans [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d0887-119">Char.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d0887-120">Para obtener una referencia desde un programa a la celda Transparency por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d0887-120">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0887-121">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d0887-121">Section index:</span></span>  <br/> |<span data-ttu-id="d0887-122">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d0887-122">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="d0887-123">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d0887-123">Row index:</span></span>  <br/> |<span data-ttu-id="d0887-124">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d0887-124">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d0887-125">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d0887-125">Cell index:</span></span>  <br/> |<span data-ttu-id="d0887-126">**visCharacterColorTrans**</span><span class="sxs-lookup"><span data-stu-id="d0887-126">**visCharacterColorTrans**</span></span> <br/> |
   

