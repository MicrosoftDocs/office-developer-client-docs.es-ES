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
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420356"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="8d49e-103">Celda PlowCode (Sección de diseño de página)</span><span class="sxs-lookup"><span data-stu-id="8d49e-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="8d49e-104">Determina si las formas colocables se desplazan cuando se coloca una forma colocable cerca de otra en la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="8d49e-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="8d49e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8d49e-105">**Value**</span></span>|<span data-ttu-id="8d49e-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d49e-106">**Description**</span></span>|<span data-ttu-id="8d49e-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="8d49e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8d49e-108">0</span><span class="sxs-lookup"><span data-stu-id="8d49e-108">0</span></span>  <br/> |<span data-ttu-id="8d49e-109">No mover formas</span><span class="sxs-lookup"><span data-stu-id="8d49e-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="8d49e-110">**visPLOPlowNone**</span><span class="sxs-lookup"><span data-stu-id="8d49e-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="8d49e-111">1 </span><span class="sxs-lookup"><span data-stu-id="8d49e-111">1</span></span>  <br/> |<span data-ttu-id="8d49e-112">Mover formas</span><span class="sxs-lookup"><span data-stu-id="8d49e-112">Move shapes</span></span>  <br/> |<span data-ttu-id="8d49e-113">**visPLOPlowAll**</span><span class="sxs-lookup"><span data-stu-id="8d49e-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d49e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8d49e-114">Remarks</span></span>

<span data-ttu-id="8d49e-115">También puede establecer el valor de esta celda en  la ficha Diseño  y enrutamiento del  cuadro de diálogo  Configurar página (en la ficha Diseño, haga clic en la flecha del programa de instalación de página) mediante la casilla de verificación Mover otras formas al colocar. </span><span class="sxs-lookup"><span data-stu-id="8d49e-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="8d49e-116">Para obtener una referencia a la celda PlowCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="8d49e-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d49e-117">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8d49e-117">Cell name:</span></span>  <br/> |<span data-ttu-id="8d49e-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="8d49e-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="8d49e-119">Para obtener una referencia desde un programa a la celda PlowCode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8d49e-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d49e-120">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8d49e-120">Section index:</span></span>  <br/> |<span data-ttu-id="8d49e-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8d49e-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8d49e-122">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8d49e-122">Row index:</span></span>  <br/> |<span data-ttu-id="8d49e-123">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="8d49e-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="8d49e-124">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8d49e-124">Cell index:</span></span>  <br/> |<span data-ttu-id="8d49e-125">**visPLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="8d49e-125">**visPLOPlowCode**</span></span> <br/> |
   

