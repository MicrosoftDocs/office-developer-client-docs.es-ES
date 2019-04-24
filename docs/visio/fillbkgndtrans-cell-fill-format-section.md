---
title: Celda FillBkgndTrans (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253230
localization_priority: Normal
ms.assetid: 87065350-ba9a-aae8-47f6-f263f6700d08
description: Determina el nivel de transparencia del color de fondo de la trama de relleno de la forma.
ms.openlocfilehash: 64c5d09fb18f089769e025893b9fac8b1878fca1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322487"
---
# <a name="fillbkgndtrans-cell-fill-format-section"></a><span data-ttu-id="9e5ab-103">Celda FillBkgndTrans (Sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="9e5ab-103">FillBkgndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="9e5ab-104">Determina el nivel de transparencia del color de fondo de la trama de relleno de la forma.</span><span class="sxs-lookup"><span data-stu-id="9e5ab-104">Determines the transparency level for the background (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="9e5ab-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="9e5ab-105">**Value**</span></span>|<span data-ttu-id="9e5ab-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9e5ab-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9e5ab-107">0 -100</span><span class="sxs-lookup"><span data-stu-id="9e5ab-107">0 - 100</span></span>  <br/> |<span data-ttu-id="9e5ab-p101">Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="9e5ab-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e5ab-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9e5ab-110">Remarks</span></span>

<span data-ttu-id="9e5ab-p102">Los valores se redondean al porcentaje medio más próximo. El valor 100% hace que sea totalmente transparente. Aunque en la página de dibujo una forma con un relleno totalmente transparente y otra sin relleno aparecen igual, la interacción con los demás objetos de la página se producirá como si su transparencia fuera del cero por ciento.</span><span class="sxs-lookup"><span data-stu-id="9e5ab-p102">Values are rounded to the nearest half percent. A value of 100% is completely transparent. Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="9e5ab-p103">También puede usar el control deslizante del cuadro de diálogo **Relleno** para establecer este valor (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Relleno** y, a continuación, en **Opciones de relleno**). Este valor controla el de las transparencias de relleno de primer y segundo plano. Para establecer estos valores de forma independiente, debe escribirlos en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="9e5ab-p103">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**). This value controls the value of both the background and foreground fill transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="9e5ab-117">Para obtener una referencia a la celda FillBkgndTrans por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="9e5ab-117">To get a reference to the FillBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e5ab-118">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="9e5ab-118">Cell name:</span></span>  <br/> |<span data-ttu-id="9e5ab-119">FillBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="9e5ab-119">FillBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="9e5ab-120">Para obtener una referencia desde un programa a la celda FillBkgndTrans por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9e5ab-120">To get a reference to the FillBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e5ab-121">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="9e5ab-121">Section index:</span></span>  <br/> |<span data-ttu-id="9e5ab-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9e5ab-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9e5ab-123">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="9e5ab-123">Row index:</span></span>  <br/> |<span data-ttu-id="9e5ab-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="9e5ab-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="9e5ab-125">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="9e5ab-125">Cell index:</span></span>  <br/> |<span data-ttu-id="9e5ab-126">**visFillBkgndTrans**</span><span class="sxs-lookup"><span data-stu-id="9e5ab-126">**visFillBkgndTrans**</span></span> <br/> |
   

