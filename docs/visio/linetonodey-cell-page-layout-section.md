---
title: Celda LineToNodeY (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251650
localization_priority: Normal
ms.assetid: 49d649e8-1603-192b-2984-e5d0b713da89
description: Determina el gálibo vertical entre todos los conectores y formas de la página de dibujo.
ms.openlocfilehash: bd5216a68abc4bcd8c3ef807b98280edb0ad29b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822471"
---
# <a name="linetonodey-cell-page-layout-section"></a><span data-ttu-id="b6c43-103">Celda LineToNodeY (sección Diseño de página)</span><span class="sxs-lookup"><span data-stu-id="b6c43-103">LineToNodeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="b6c43-104">Determina el gálibo vertical entre todos los conectores y formas de la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="b6c43-104">Determines the vertical clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6c43-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6c43-105">Remarks</span></span>

<span data-ttu-id="b6c43-p101">También puede establecer el valor de esta celda en el cuadro de diálogo **Espaciado del diseño y el enrutamiento**. (En la ficha **Diseño**, haga clic en la flecha de **Configurar página**, haga clic en **Diseño y enrutamiento** y, a continuación, en **Espaciado**).</span><span class="sxs-lookup"><span data-stu-id="b6c43-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="b6c43-108">Para obtener una referencia a la celda LineToNodeY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="b6c43-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6c43-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="b6c43-109">Cell name:</span></span>  <br/> | <span data-ttu-id="b6c43-110">LineToNodeY</span><span class="sxs-lookup"><span data-stu-id="b6c43-110">LineToNodeY</span></span>  <br/> |
   
<span data-ttu-id="b6c43-111">Para obtener una referencia desde un programa a la celda LineToNodeY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b6c43-111">To get a reference to the LineToNodeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6c43-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="b6c43-112">Section index:</span></span>  <br/> |<span data-ttu-id="b6c43-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b6c43-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b6c43-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="b6c43-114">Row index:</span></span>  <br/> |<span data-ttu-id="b6c43-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b6c43-115">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="b6c43-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="b6c43-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b6c43-117">**visPLOLineToNodeY**</span><span class="sxs-lookup"><span data-stu-id="b6c43-117">**visPLOLineToNodeY**</span></span> <br/> |
   

