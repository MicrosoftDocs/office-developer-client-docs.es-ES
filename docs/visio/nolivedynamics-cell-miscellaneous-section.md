---
title: Celda NoLiveDynamics (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm720
localization_priority: Normal
ms.assetid: d1c4b9d9-6d64-8ed1-9fc6-2dbf829a75b5
description: Determina si una forma cambia de tamaño o gira dinámicamente a medida que el usuario trabaja con ella.
ms.openlocfilehash: 043571243fe3698561bee8632e7fd18db04c9330
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822674"
---
# <a name="nolivedynamics-cell-miscellaneous-section"></a><span data-ttu-id="6b82f-103">Celda NoLiveDynamics (Sección de varios)</span><span class="sxs-lookup"><span data-stu-id="6b82f-103">NoLiveDynamics Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="6b82f-104">Determina si una forma cambia de tamaño o gira dinámicamente a medida que el usuario trabaja con ella.</span><span class="sxs-lookup"><span data-stu-id="6b82f-104">Determines whether a shape dynamically resizes or rotates as you are manipulating it.</span></span>
  
|<span data-ttu-id="6b82f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6b82f-105">**Value**</span></span>|<span data-ttu-id="6b82f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b82f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6b82f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="6b82f-107">TRUE</span></span>  <br/> | <span data-ttu-id="6b82f-108">La forma no se actualiza dinámicamente mientras el usuario trabaja con ella.</span><span class="sxs-lookup"><span data-stu-id="6b82f-108">Do not dynamically update the shape while you are manipulating it.</span></span>  <br/> |
| <span data-ttu-id="6b82f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="6b82f-109">FALSE</span></span>  <br/> | <span data-ttu-id="6b82f-110">La forma se actualiza dinámicamente mientras el usuario trabaja con ella.</span><span class="sxs-lookup"><span data-stu-id="6b82f-110">Dynamically update the shape while you are manipulating it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b82f-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b82f-111">Remarks</span></span>

<span data-ttu-id="6b82f-p101">A medida que cambia de tamaño o gira una forma bidimensional (2D) sin dinámica activa, puede ver un cuadro de selección. Si la forma es unidimensional (1D), el efecto visual se basa en el valor de la celda DynFeedback.</span><span class="sxs-lookup"><span data-stu-id="6b82f-p101">As you resize or rotate a two-dimensional (2-D) shape without live dynamics, you see a selection box. If the shape is one-dimensional (1-D), the visual feedback is based on the value of the DynFeedback cell.</span></span>
  
<span data-ttu-id="6b82f-114">Para obtener una referencia a la celda NoLiveDymanics por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="6b82f-114">To get a reference to the NoLiveDynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b82f-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="6b82f-115">Cell name:</span></span>  <br/> | <span data-ttu-id="6b82f-116">NoLiveDynamics</span><span class="sxs-lookup"><span data-stu-id="6b82f-116">NoLiveDynamics</span></span>  <br/> |
   
<span data-ttu-id="6b82f-117">Para obtener una referencia a la celda NoLiveDynamics por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6b82f-117">To get a reference to the NoLiveDynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b82f-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="6b82f-118">Section index:</span></span>  <br/> |<span data-ttu-id="6b82f-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6b82f-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6b82f-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="6b82f-120">Row index:</span></span>  <br/> |<span data-ttu-id="6b82f-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="6b82f-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="6b82f-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="6b82f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="6b82f-123">**visNoLiveDynamics**</span><span class="sxs-lookup"><span data-stu-id="6b82f-123">**visNoLiveDynamics**</span></span> <br/> |
   

