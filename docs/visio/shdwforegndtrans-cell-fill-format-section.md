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
ms.openlocfilehash: 5fd385fc2f46f1ff8eedc961833813ec16ba7b73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823202"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a><span data-ttu-id="ddbf7-103">Celda ShdwForegndTrans (Sección de formato de relleno)</span><span class="sxs-lookup"><span data-stu-id="ddbf7-103">ShdwForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="ddbf7-104">Determina el nivel de transparencia del color utilizado para el primer plano (trazo) de la trama de relleno sombreado de la forma.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-104">Determines the transparency level for the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
|<span data-ttu-id="ddbf7-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ddbf7-105">**Value**</span></span>|<span data-ttu-id="ddbf7-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ddbf7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ddbf7-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="ddbf7-107">0 - 100</span></span>  <br/> |<span data-ttu-id="ddbf7-p101">Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="ddbf7-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddbf7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddbf7-110">Remarks</span></span>

<span data-ttu-id="ddbf7-111">Los valores se redondean al porcentaje medio más próximo.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="ddbf7-112">Un valor de 100% es completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="ddbf7-113">Aunque una sombra que tiene un relleno transparente completamente el mismo en la página de dibujo aparece como una sombra que no tiene relleno, interactúa con otros objetos en la página de la misma manera como si su transparencia fuera 0%.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-113">Although a shadow that has a completely transparent fill appears the same on the drawing page as a shadow that has no fill, it interacts with other objects on the page in the same ways as if its transparency were 0%.</span></span>
  
<span data-ttu-id="ddbf7-114">También puede establecer este valor mediante el control deslizante en el cuadro de diálogo **sombra** (en la ficha **Inicio** , en el grupo **forma** , haga clic en **sombra**y, a continuación, haga clic en **Opciones de sombra**).</span><span class="sxs-lookup"><span data-stu-id="ddbf7-114">You can also set this value by using the slider control in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span> <span data-ttu-id="ddbf7-115">Este valor controla el valor de transparencia de sombra de fondo y de primer plano.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-115">This value controls the value of both the background and foreground shadow transparencies.</span></span> <span data-ttu-id="ddbf7-116">Para establecer estos valores de forma independiente, debe escribir en la ventana ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-116">To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="ddbf7-117">Para obtener una referencia a la celda ShdwForegndTrans por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="ddbf7-117">To get a reference to the ShdwForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddbf7-118">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="ddbf7-118">Cell name:</span></span>  <br/> |<span data-ttu-id="ddbf7-119">ShdwForegndTrans</span><span class="sxs-lookup"><span data-stu-id="ddbf7-119">ShdwForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="ddbf7-120">Para obtener una referencia a la celda ShdwForegndTrans por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ddbf7-120">To get a reference to the ShdwForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddbf7-121">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="ddbf7-121">Section index:</span></span>  <br/> |<span data-ttu-id="ddbf7-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ddbf7-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ddbf7-123">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="ddbf7-123">Row index:</span></span>  <br/> |<span data-ttu-id="ddbf7-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="ddbf7-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="ddbf7-125">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="ddbf7-125">Cell index:</span></span>  <br/> |<span data-ttu-id="ddbf7-126">**visFillShdwForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="ddbf7-126">**visFillShdwForegndTrans**</span></span> <br/> |
   

