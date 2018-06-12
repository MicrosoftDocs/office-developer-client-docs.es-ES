---
title: Celda PlowCode (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Determina si las formas colocables se desplazan cuando se coloca una forma colocable cerca de otra en la página de dibujo.
ms.openlocfilehash: e180ce679f280cbccbda80b67170f2f26473bd8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822781"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="f0537-103">Celda PlowCode (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="f0537-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="f0537-104">Determina si las formas colocables se desplazan cuando se coloca una forma colocable cerca de otra en la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="f0537-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="f0537-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f0537-105">**Value**</span></span>|<span data-ttu-id="f0537-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0537-106">**Description**</span></span>|<span data-ttu-id="f0537-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="f0537-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f0537-108">0</span><span class="sxs-lookup"><span data-stu-id="f0537-108">0</span></span>  <br/> |<span data-ttu-id="f0537-109">No mover formas</span><span class="sxs-lookup"><span data-stu-id="f0537-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="f0537-110">**visPLOPlowNone**</span><span class="sxs-lookup"><span data-stu-id="f0537-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="f0537-111">1</span><span class="sxs-lookup"><span data-stu-id="f0537-111">1</span></span>  <br/> |<span data-ttu-id="f0537-112">Mover formas</span><span class="sxs-lookup"><span data-stu-id="f0537-112">Move shapes</span></span>  <br/> |<span data-ttu-id="f0537-113">**visPLOPlowAll**</span><span class="sxs-lookup"><span data-stu-id="f0537-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0537-114">Notas</span><span class="sxs-lookup"><span data-stu-id="f0537-114">Remarks</span></span>

<span data-ttu-id="f0537-115">También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** ) mediante el uso de la casilla de verificación **mover las otras formas al colocar** .</span><span class="sxs-lookup"><span data-stu-id="f0537-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="f0537-116">Para obtener una referencia a la celda PlowCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="f0537-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0537-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f0537-117">Cell name:</span></span>  <br/> |<span data-ttu-id="f0537-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="f0537-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="f0537-119">Para obtener una referencia a la celda PlowCode por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f0537-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0537-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f0537-120">Section index:</span></span>  <br/> |<span data-ttu-id="f0537-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f0537-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f0537-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f0537-122">Row index:</span></span>  <br/> |<span data-ttu-id="f0537-123">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="f0537-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="f0537-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f0537-124">Cell index:</span></span>  <br/> |<span data-ttu-id="f0537-125">**visPLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="f0537-125">**visPLOPlowCode**</span></span> <br/> |
   

