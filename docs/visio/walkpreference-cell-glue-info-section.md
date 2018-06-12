---
title: Celda WalkPreference (Sección de información de pegado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
localization_priority: Normal
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: Determina si un extremo de una forma 1D se mueve a un punto de conexión horizontal o vertical de la forma a la que se pega, cuando se usa pegado dinámico y la forma se mueve a una posición ambigua. De forma predeterminada, ambos extremos de la forma 1D se mueven a los puntos de conexión horizontales.
ms.openlocfilehash: cd64a67de6ec914ad1bde86cdac829f6c12cebe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823535"
---
# <a name="walkpreference-cell-glue-info-section"></a><span data-ttu-id="37823-104">Celda WalkPreference (Sección de información de pegado)</span><span class="sxs-lookup"><span data-stu-id="37823-104">WalkPreference Cell (Glue Info Section)</span></span>

<span data-ttu-id="37823-p102">Determina si un extremo de una forma 1D se mueve a un punto de conexión horizontal o vertical de la forma a la que se pega, cuando se usa pegado dinámico y la forma se mueve a una posición ambigua. De forma predeterminada, ambos extremos de la forma 1D se mueven a los puntos de conexión horizontales.</span><span class="sxs-lookup"><span data-stu-id="37823-p102">Determines whether an endpoint of a 1-D shape moves to a horizontal or vertical connection point on the shape it is glued to, using dynamic glue, when the shape is moved to an ambiguous position. By default, both endpoints of the 1-D shape move to horizontal connection points.</span></span>
  
|<span data-ttu-id="37823-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="37823-107">**Value**</span></span>|<span data-ttu-id="37823-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37823-108">**Description**</span></span>|<span data-ttu-id="37823-109">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="37823-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="37823-110">1</span><span class="sxs-lookup"><span data-stu-id="37823-110">1</span></span>  <br/> | <span data-ttu-id="37823-111">El punto inicial de la forma 1D se mueve a un punto de conexión vertical y el extremo se mueve a un punto de conexión horizontal (conexiones entre el borde superior y un lado, o entre el borde inferior y un lado).</span><span class="sxs-lookup"><span data-stu-id="37823-111">The begin point of the 1-D shape moves to a vertical connection point, and the endpoint moves to a horizontal connection point (top-to-side or bottom-to-side connections).</span></span>  <br/> |<span data-ttu-id="37823-112">**visWalkPrefBegNS**</span><span class="sxs-lookup"><span data-stu-id="37823-112">**visWalkPrefBegNS**</span></span> <br/> |
| <span data-ttu-id="37823-113">2</span><span class="sxs-lookup"><span data-stu-id="37823-113">2</span></span>  <br/> | <span data-ttu-id="37823-114">El punto inicial de la forma 1D se mueve a un punto de conexión horizontal y el extremo se mueve a un punto de conexión vertical (conexiones entre un lado y el borde superior, o entre un lado y el borde inferior).</span><span class="sxs-lookup"><span data-stu-id="37823-114">The begin point of the 1-D shape moves to a horizontal connection point, and the endpoint moves to a vertical connection point (side-to-top or side-to-bottom connections).</span></span>  <br/> |<span data-ttu-id="37823-115">**visWalkPrefEndNS**</span><span class="sxs-lookup"><span data-stu-id="37823-115">**visWalkPrefEndNS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37823-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37823-116">Remarks</span></span>

<span data-ttu-id="37823-p103">Esta celda no tiene ningún efecto en los conectores dinámicos. El comportamiento de los conectores dinámicos viene determinado por su estilo de enrutamiento. Vea la celda RouteStyle para ver el estilo de enrutamiento predeterminado para los conectores dinámicos de una página o la celda ShapeRouteStyle para ver el estilo de enrutamiento de un conector dinámico determinado.</span><span class="sxs-lookup"><span data-stu-id="37823-p103">This cell has no effect on dynamic connectors. A dynamic connector's behavior is determined by its routing style. See the RouteStyle cell for the default routing style for dynamic connectors on a page, or the ShapeRouteStyle for the routing style of a particular dynamic connector.</span></span>
  
<span data-ttu-id="37823-120">Para obtener una referencia a la celda WalkPreference por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="37823-120">To get a reference to the WalkPreference cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37823-121">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="37823-121">Cell name:</span></span>  <br/> | <span data-ttu-id="37823-122">WalkPreference</span><span class="sxs-lookup"><span data-stu-id="37823-122">WalkPreference</span></span>  <br/> |
   
<span data-ttu-id="37823-123">Para obtener una referencia a la celda WalkPreference por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="37823-123">To get a reference to the WalkPreference cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="37823-124">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="37823-124">Section index:</span></span>  <br/> |<span data-ttu-id="37823-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37823-125">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="37823-126">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="37823-126">Row index:</span></span>  <br/> |<span data-ttu-id="37823-127">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="37823-127">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="37823-128">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="37823-128">Cell index:</span></span>  <br/> |<span data-ttu-id="37823-129">**visWalkPref**</span><span class="sxs-lookup"><span data-stu-id="37823-129">**visWalkPref**</span></span> <br/> |
   

