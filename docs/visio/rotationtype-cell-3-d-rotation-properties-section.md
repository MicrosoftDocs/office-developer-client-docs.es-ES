---
title: Celda RotationType (sección Propiedades de rotación 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Determina si la forma sigue una rotación paralela, una rotación de perspectiva o una rotación oblicua, como un entero de 0 a 6.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422946"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="3c36f-103">Celda RotationType (sección Propiedades de rotación 3D)</span><span class="sxs-lookup"><span data-stu-id="3c36f-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="3c36f-104">Determina si la forma sigue una rotación paralela, una rotación de perspectiva o una rotación oblicua, como un entero de 0 a 6.</span><span class="sxs-lookup"><span data-stu-id="3c36f-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="3c36f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3c36f-105">**Value**</span></span>|<span data-ttu-id="3c36f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c36f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3c36f-107">0</span><span class="sxs-lookup"><span data-stu-id="3c36f-107">0</span></span>  <br/> |<span data-ttu-id="3c36f-108">La forma no tiene ninguna rotación.</span><span class="sxs-lookup"><span data-stu-id="3c36f-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="3c36f-109">1</span><span class="sxs-lookup"><span data-stu-id="3c36f-109">1</span></span>  <br/> |<span data-ttu-id="3c36f-110">La forma tiene un giro paralelo.</span><span class="sxs-lookup"><span data-stu-id="3c36f-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="3c36f-111">2</span><span class="sxs-lookup"><span data-stu-id="3c36f-111">2</span></span>  <br/> |<span data-ttu-id="3c36f-112">La forma tiene un giro de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="3c36f-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="3c36f-113">3</span><span class="sxs-lookup"><span data-stu-id="3c36f-113">3</span></span>  <br/> |<span data-ttu-id="3c36f-114">La forma tiene un giro oblicua superior izquierdo.</span><span class="sxs-lookup"><span data-stu-id="3c36f-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="3c36f-115">4 </span><span class="sxs-lookup"><span data-stu-id="3c36f-115">4</span></span>  <br/> |<span data-ttu-id="3c36f-116">La forma tiene un giro oblicua superior derecho.</span><span class="sxs-lookup"><span data-stu-id="3c36f-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="3c36f-117">5 </span><span class="sxs-lookup"><span data-stu-id="3c36f-117">5</span></span>  <br/> |<span data-ttu-id="3c36f-118">La forma tiene un giro oblicua inferior izquierdo.</span><span class="sxs-lookup"><span data-stu-id="3c36f-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="3c36f-119">6 </span><span class="sxs-lookup"><span data-stu-id="3c36f-119">6</span></span>  <br/> |<span data-ttu-id="3c36f-120">La forma tiene un giro oblicua inferior derecho.</span><span class="sxs-lookup"><span data-stu-id="3c36f-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c36f-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c36f-121">Remarks</span></span>

<span data-ttu-id="3c36f-122">Para obtener una referencia a la **celda RotationType** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la **propiedad CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="3c36f-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c36f-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="3c36f-123">Cell name:</span></span>  <br/> |<span data-ttu-id="3c36f-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="3c36f-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="3c36f-125">Para obtener una referencia desde un programa a **la celda RotationType** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3c36f-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c36f-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="3c36f-126">Section index:</span></span>  <br/> |<span data-ttu-id="3c36f-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3c36f-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3c36f-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="3c36f-128">Row index:</span></span>  <br/> |<span data-ttu-id="3c36f-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="3c36f-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="3c36f-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="3c36f-130">Cell index:</span></span>  <br/> |<span data-ttu-id="3c36f-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="3c36f-131">**visRotationType**</span></span> <br/> |
   

