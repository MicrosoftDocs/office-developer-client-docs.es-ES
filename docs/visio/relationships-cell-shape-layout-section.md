---
title: Celda Relationships (sección de diseño de la forma [Shape Layout])
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
localization_priority: Normal
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: Almacena las relaciones entre contenedores, listas, llamadas y formas.
ms.openlocfilehash: b270366fe1045aea3d628150c82e7fd798fa21df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406412"
---
# <a name="relationships-cell-shape-layout-section"></a><span data-ttu-id="02a24-103">Celda Relationships (sección de diseño de la forma [Shape Layout])</span><span class="sxs-lookup"><span data-stu-id="02a24-103">Relationships Cell (Shape Layout Section)</span></span>

<span data-ttu-id="02a24-104">Almacena las relaciones entre contenedores, listas, llamadas y formas.</span><span class="sxs-lookup"><span data-stu-id="02a24-104">Stores the relationships between containers, lists, callouts, and shapes.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="02a24-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02a24-105">Remarks</span></span>

 <span data-ttu-id="02a24-106">Microsoft Visio usa la celda Relationships para almacenar las relaciones que implican esta forma.</span><span class="sxs-lookup"><span data-stu-id="02a24-106">Microsoft Visio uses the Relationships cell to store the relationships that involve this shape.</span></span> <span data-ttu-id="02a24-107">Se usa una serie de funciones DEPENDSON, con los parámetros mostrados, para representar las relaciones con esta forma, tal y como refleja la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="02a24-107">A series of DEPENDSON functions, with the parameters shown, are used to represent relationships with this shape, as shown in the following table.</span></span> 
  
|<span data-ttu-id="02a24-108">**Primer parámetro**</span><span class="sxs-lookup"><span data-stu-id="02a24-108">**First parameter**</span></span>|<span data-ttu-id="02a24-109">**Parámetros adicionales**</span><span class="sxs-lookup"><span data-stu-id="02a24-109">**Additional parameters**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02a24-110">1 </span><span class="sxs-lookup"><span data-stu-id="02a24-110">1</span></span>  <br/> |<span data-ttu-id="02a24-111">Formas que son miembros de este contenedor.</span><span class="sxs-lookup"><span data-stu-id="02a24-111">Shapes that are members of this container.</span></span>  <br/> |
|<span data-ttu-id="02a24-112">2 </span><span class="sxs-lookup"><span data-stu-id="02a24-112">2</span></span>  <br/> |<span data-ttu-id="02a24-113">Formas que son miembros de esta lista.</span><span class="sxs-lookup"><span data-stu-id="02a24-113">Shapes that are members of this list.</span></span>  <br/> |
|<span data-ttu-id="02a24-114">3 </span><span class="sxs-lookup"><span data-stu-id="02a24-114">3</span></span>  <br/> |<span data-ttu-id="02a24-115">Llamadas asociadas con esta forma.</span><span class="sxs-lookup"><span data-stu-id="02a24-115">Callouts that are associated with this shape.</span></span>  <br/> |
|<span data-ttu-id="02a24-116">4 </span><span class="sxs-lookup"><span data-stu-id="02a24-116">4</span></span>  <br/> |<span data-ttu-id="02a24-117">Contenedores de los que esta forma es miembro.</span><span class="sxs-lookup"><span data-stu-id="02a24-117">Containers that this shape is a member of.</span></span>  <br/> |
|<span data-ttu-id="02a24-118">5 </span><span class="sxs-lookup"><span data-stu-id="02a24-118">5</span></span>  <br/> |<span data-ttu-id="02a24-119">Lista de la que este elemento de lista es miembro.</span><span class="sxs-lookup"><span data-stu-id="02a24-119">List that this list item is a member of.</span></span>  <br/> |
|<span data-ttu-id="02a24-120">6 </span><span class="sxs-lookup"><span data-stu-id="02a24-120">6</span></span>  <br/> |<span data-ttu-id="02a24-121">Formas asociadas con esta llamada.</span><span class="sxs-lookup"><span data-stu-id="02a24-121">Shape associated with this callout.</span></span>  <br/> |
|<span data-ttu-id="02a24-122">7 </span><span class="sxs-lookup"><span data-stu-id="02a24-122">7</span></span>  <br/> |<span data-ttu-id="02a24-123">Contenedor en cuyo borde límite izquierdo se asienta esta forma.</span><span class="sxs-lookup"><span data-stu-id="02a24-123">Container on the left boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="02a24-124">8 </span><span class="sxs-lookup"><span data-stu-id="02a24-124">8</span></span>  <br/> |<span data-ttu-id="02a24-125">Contenedor en cuyo borde límite derecho se asienta esta forma.</span><span class="sxs-lookup"><span data-stu-id="02a24-125">Container on the right boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="02a24-126">9 </span><span class="sxs-lookup"><span data-stu-id="02a24-126">9</span></span>  <br/> |<span data-ttu-id="02a24-127">Contenedor en cuyo borde límite superior se asienta esta forma.</span><span class="sxs-lookup"><span data-stu-id="02a24-127">Container on the top boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="02a24-128">10  </span><span class="sxs-lookup"><span data-stu-id="02a24-128">10</span></span>  <br/> |<span data-ttu-id="02a24-129">Contenedor en cuyo borde límite inferior se asienta esta forma.</span><span class="sxs-lookup"><span data-stu-id="02a24-129">Container on the bottom boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="02a24-130">11</span><span class="sxs-lookup"><span data-stu-id="02a24-130">11</span></span>  <br/> |<span data-ttu-id="02a24-131">Lista a la que esta lista se superpone.</span><span class="sxs-lookup"><span data-stu-id="02a24-131">List that this list overlaps.</span></span>  <br/> |
   
<span data-ttu-id="02a24-132">Para obtener una referencia a la celda Relationships por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="02a24-132">To get a reference to the Relationships cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02a24-133">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="02a24-133">Cell name:</span></span>  <br/> |<span data-ttu-id="02a24-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="02a24-134">Relationships</span></span>  <br/> |
   
<span data-ttu-id="02a24-135">Para obtener una referencia desde un programa a la celda Relationships por su índice, use la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="02a24-135">To get a reference to the Relationships cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02a24-136">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="02a24-136">Section index:</span></span>  <br/> |<span data-ttu-id="02a24-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="02a24-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="02a24-138">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="02a24-138">Row index:</span></span>  <br/> |<span data-ttu-id="02a24-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="02a24-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="02a24-140">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="02a24-140">Cell index:</span></span>  <br/> |<span data-ttu-id="02a24-141">**visSLORelationships**</span><span class="sxs-lookup"><span data-stu-id="02a24-141">**visSLORelationships**</span></span> <br/> |
   

