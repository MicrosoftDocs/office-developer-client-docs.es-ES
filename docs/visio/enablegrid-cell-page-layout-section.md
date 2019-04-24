---
title: Celda EnableGrid (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Determina si la aplicación dispone las formas basándose en una cuadrícula de página, interna e invisible, cuando se configura el diseño en el cuadro de diálogo Configurar diseño. (En la ficha Diseño, en el grupo Diseño, haga clic en Redistribuir página y, a continuación, en Más opciones de diseño).
ms.openlocfilehash: 11299ca7c9b0ea050542baf97e2cab3a27fa52ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345559"
---
# <a name="enablegrid-cell-page-layout-section"></a><span data-ttu-id="39148-104">Celda EnableGrid (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="39148-104">EnableGrid Cell (Page Layout Section)</span></span>

<span data-ttu-id="39148-p102">Determina si la aplicación dispone las formas basándose en una cuadrícula de página, interna e invisible, cuando se configura el diseño en el cuadro de diálogo **Configurar diseño**. (En la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).
</span><span class="sxs-lookup"><span data-stu-id="39148-p102">Determines whether the application lays out shapes based on an internal, invisible page grid when you configure the layout in the **Configure Layout** dialog box. (On the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**.)</span></span>
  
|<span data-ttu-id="39148-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="39148-107">**Value**</span></span>|<span data-ttu-id="39148-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39148-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39148-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="39148-109">TRUE</span></span>  <br/> |<span data-ttu-id="39148-110">Utilizar la cuadrícula de página interna.</span><span class="sxs-lookup"><span data-stu-id="39148-110">Use the internal page grid.</span></span>  <br/> |
|<span data-ttu-id="39148-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="39148-111">FALSE</span></span>  <br/> |<span data-ttu-id="39148-112">No utilizar la cuadrícula de página interna.</span><span class="sxs-lookup"><span data-stu-id="39148-112">Do not use the internal page grid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39148-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39148-113">Remarks</span></span>

<span data-ttu-id="39148-p103">Esta cuadrícula de página se crea con los valores de **Espacio entre formas** y **Tamaño promedio de las formas** en el cuadro de diálogo **Espaciado del diseño y el enrutamiento**. (En la ficha **Diseño**, haga clic en la flecha de **Configurar página**, en **Diseño y enrutamiento** y, a continuación, en **Espaciado**).</span><span class="sxs-lookup"><span data-stu-id="39148-p103">You create this page grid by using the **Space between shapes** and the **Average shape size** values in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span> 
  
<span data-ttu-id="39148-116">Si esta característica está habilitada, la aplicación alinea el punto central de cada forma colocable con el punto central de uno de los bloques de la cuadrícula de página interna.</span><span class="sxs-lookup"><span data-stu-id="39148-116">When you enable this feature, the application aligns each placeable shape's center point with the center of a block on the internal page grid.</span></span> 
  
<span data-ttu-id="39148-117">Para obtener una referencia a la celda EnableGrid por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="39148-117">To get a reference to the EnableGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39148-118">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="39148-118">Cell name:</span></span>  <br/> |<span data-ttu-id="39148-119">EnableGrid</span><span class="sxs-lookup"><span data-stu-id="39148-119">EnableGrid</span></span>  <br/> |
   
<span data-ttu-id="39148-120">Para obtener una referencia desde un programa a la celda EnableGrid por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="39148-120">To get a reference to the EnableGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="39148-121">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="39148-121">Section index:</span></span>  <br/> |<span data-ttu-id="39148-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="39148-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="39148-123">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="39148-123">Row index:</span></span>  <br/> |<span data-ttu-id="39148-124">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="39148-124">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="39148-125">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="39148-125">Cell index:</span></span>  <br/> |<span data-ttu-id="39148-126">**visPLOEnableGrid**</span><span class="sxs-lookup"><span data-stu-id="39148-126">**visPLOEnableGrid**</span></span> <br/> |
   

