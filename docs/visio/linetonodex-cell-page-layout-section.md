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
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="a8b1e-103">Celda LineToNodeX (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="a8b1e-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="a8b1e-104">Determina el gálibo horizontal entre todos los conectores y formas de la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="a8b1e-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8b1e-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8b1e-105">Remarks</span></span>

<span data-ttu-id="a8b1e-106">También puede establecer el valor de esta celda en el cuadro de diálogo **Diseño de espaciado y el enrutamiento** .</span><span class="sxs-lookup"><span data-stu-id="a8b1e-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="a8b1e-107">(En la ficha **Diseño** , haga clic en la flecha de **Configurar página** , haga clic en **Diseño y enrutamiento**y, a continuación, haga clic en **Espaciado**).</span><span class="sxs-lookup"><span data-stu-id="a8b1e-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="a8b1e-108">Para obtener una referencia a la celda LineToNodeY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="a8b1e-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8b1e-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="a8b1e-109">Cell name:</span></span>  <br/> |<span data-ttu-id="a8b1e-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="a8b1e-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="a8b1e-111">Para obtener una referencia a la celda LineToNodeX por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a8b1e-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8b1e-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="a8b1e-112">Section index:</span></span>  <br/> |<span data-ttu-id="a8b1e-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a8b1e-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a8b1e-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="a8b1e-114">Row index:</span></span>  <br/> |<span data-ttu-id="a8b1e-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a8b1e-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a8b1e-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="a8b1e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a8b1e-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="a8b1e-117">**visPLOLineToNodeX**</span></span> <br/> |
   

