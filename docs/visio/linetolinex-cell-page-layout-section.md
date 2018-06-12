---
title: Celda LineToLineX (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm565
localization_priority: Normal
ms.assetid: f6b461fe-56ac-4c0e-31cd-6b3c1075db6e
description: Determina el gálibo horizontal entre todos los conectores de la página de dibujo.
ms.openlocfilehash: aa6476eab9d5bcf7aab12235fd23f0f5675d6ad5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822463"
---
# <a name="linetolinex-cell-page-layout-section"></a><span data-ttu-id="d4ada-103">Celda LineToLineX (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="d4ada-103">LineToLineX Cell (Page Layout Section)</span></span>

<span data-ttu-id="d4ada-104">Determina el gálibo horizontal entre todos los conectores de la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="d4ada-104">Determines the horizontal clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d4ada-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4ada-105">Remarks</span></span>

<span data-ttu-id="d4ada-106">También puede establecer el valor de esta celda en el cuadro de diálogo **Diseño de espaciado y el enrutamiento** .</span><span class="sxs-lookup"><span data-stu-id="d4ada-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="d4ada-107">(En la ficha **Diseño** , haga clic en la flecha de **Configurar página** , haga clic en **Diseño y enrutamiento**y, a continuación, haga clic en **Espaciado**).</span><span class="sxs-lookup"><span data-stu-id="d4ada-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="d4ada-108">Para obtener una referencia a la celda LineToLineX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="d4ada-108">To get a reference to the LineToLineX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4ada-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d4ada-109">Cell name:</span></span>  <br/> |<span data-ttu-id="d4ada-110">LineToLineX</span><span class="sxs-lookup"><span data-stu-id="d4ada-110">LineToLineX</span></span>  <br/> |
   
<span data-ttu-id="d4ada-111">Para obtener una referencia a la celda LineToLineX por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d4ada-111">To get a reference to the LineToLineX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4ada-112">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d4ada-112">Section index:</span></span>  <br/> |<span data-ttu-id="d4ada-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d4ada-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d4ada-114">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d4ada-114">Row index:</span></span>  <br/> |<span data-ttu-id="d4ada-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="d4ada-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="d4ada-116">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d4ada-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d4ada-117">**visPLOLineToLineX**</span><span class="sxs-lookup"><span data-stu-id="d4ada-117">**visPLOLineToLineX**</span></span> <br/> |
   

