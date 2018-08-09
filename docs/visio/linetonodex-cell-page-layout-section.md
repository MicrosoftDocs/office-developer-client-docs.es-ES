---
title: Celda LineToNodeX (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm575
localization_priority: Normal
ms.assetid: 9d58e23e-b411-c5c1-b785-5014488d42c8
description: Determina el gálibo horizontal entre todos los conectores y formas de la página de dibujo.
ms.openlocfilehash: 75f7e8150711421138a01175be34003d124e88ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822472"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="a2ce7-103">Celda LineToNodeX (sección Diseño de página)</span><span class="sxs-lookup"><span data-stu-id="a2ce7-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="a2ce7-104">Determina el gálibo horizontal entre todos los conectores y formas de la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2ce7-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2ce7-105">Remarks</span></span>

<span data-ttu-id="a2ce7-p101">También puede establecer el valor de esta celda en el cuadro de diálogo **Espaciado del diseño y el enrutamiento**. (En la ficha **Diseño**, haga clic en la flecha de **Configurar página**, haga clic en **Diseño y enrutamiento** y, a continuación, en **Espaciado**).</span><span class="sxs-lookup"><span data-stu-id="a2ce7-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="a2ce7-108">Para obtener una referencia a la celda LineToNodeY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="a2ce7-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2ce7-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a2ce7-109">Cell name:</span></span>  <br/> |<span data-ttu-id="a2ce7-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="a2ce7-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="a2ce7-111">Para obtener una referencia desde un programa a la celda LineToNodeX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a2ce7-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2ce7-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a2ce7-112">Section index:</span></span>  <br/> |<span data-ttu-id="a2ce7-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a2ce7-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a2ce7-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a2ce7-114">Row index:</span></span>  <br/> |<span data-ttu-id="a2ce7-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a2ce7-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a2ce7-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a2ce7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a2ce7-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="a2ce7-117">**visPLOLineToNodeX**</span></span> <br/> |
   

