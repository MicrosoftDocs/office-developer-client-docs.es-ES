---
title: Celda ShdwForegndTrans (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Determina el nivel de transparencia del color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.
ms.openlocfilehash: 0ef3ce525edcce4ccd61f36649ead512545eef58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349101"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a><span data-ttu-id="f3a93-103">Celda ShdwForegndTrans (Sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="f3a93-103">ShdwForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="f3a93-104">Determina el nivel de transparencia del color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.</span><span class="sxs-lookup"><span data-stu-id="f3a93-104">Determines the transparency level for the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
|<span data-ttu-id="f3a93-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="f3a93-105">**Value**</span></span>|<span data-ttu-id="f3a93-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3a93-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3a93-107">0 -100</span><span class="sxs-lookup"><span data-stu-id="f3a93-107">0 - 100</span></span>  <br/> |<span data-ttu-id="f3a93-p101">Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="f3a93-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3a93-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3a93-110">Remarks</span></span>

<span data-ttu-id="f3a93-111">Los valores se redondean al medio porcentaje más próximo.</span><span class="sxs-lookup"><span data-stu-id="f3a93-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="f3a93-112">El valor 100% hace que sea totalmente transparente.</span><span class="sxs-lookup"><span data-stu-id="f3a93-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="f3a93-113">Aunque una sombra que tiene un relleno completamente transparente aparece de la misma forma en la página de dibujo que una sombra sin relleno, interactúa con otros objetos de la página de la misma manera que si su transparencia fuera del 0%.</span><span class="sxs-lookup"><span data-stu-id="f3a93-113">Although a shadow that has a completely transparent fill appears the same on the drawing page as a shadow that has no fill, it interacts with other objects on the page in the same ways as if its transparency were 0%.</span></span>
  
<span data-ttu-id="f3a93-p103">También puede usar el control deslizante del cuadro de diálogo **Sombra** para establecer este valor (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Sombra** y, a continuación, en **Opciones de sombra**). Este valor controla el valor de las transparencias de sombra de primer y segundo plano. Para establecer estos valores de forma independiente, debe escribirlos en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="f3a93-p103">You can also set this value by using the slider control in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**). This value controls the value of both the background and foreground shadow transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="f3a93-117">Para obtener una referencia a la celda ShdwForegndTrans por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="f3a93-117">To get a reference to the ShdwForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3a93-118">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f3a93-118">Cell name:</span></span>  <br/> |<span data-ttu-id="f3a93-119">ShdwForegndTrans</span><span class="sxs-lookup"><span data-stu-id="f3a93-119">ShdwForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="f3a93-120">Para obtener una referencia desde un programa a la celda ShdwForegndTrans por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f3a93-120">To get a reference to the ShdwForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3a93-121">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f3a93-121">Section index:</span></span>  <br/> |<span data-ttu-id="f3a93-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f3a93-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f3a93-123">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f3a93-123">Row index:</span></span>  <br/> |<span data-ttu-id="f3a93-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="f3a93-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="f3a93-125">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f3a93-125">Cell index:</span></span>  <br/> |<span data-ttu-id="f3a93-126">**visFillShdwForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="f3a93-126">**visFillShdwForegndTrans**</span></span> <br/> |
   

