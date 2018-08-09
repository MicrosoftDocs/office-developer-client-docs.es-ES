---
title: Celda RotationType (sección de propiedades de giro 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Determina si la forma sigue un giro paralelo, una rotación en perspectiva o un giro oblicua, como un número entero de 0 a 6.
ms.openlocfilehash: 85effcef3969d7b7c57551ec88710ba84b3fc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823040"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a><span data-ttu-id="72f75-103">Celda RotationType (sección de propiedades de giro 3D)</span><span class="sxs-lookup"><span data-stu-id="72f75-103">RotationType Cell (3-D Rotation Properties Section)</span></span>

<span data-ttu-id="72f75-104">Determina si la forma sigue un giro paralelo, una rotación en perspectiva o un giro oblicua, como un número entero de 0 a 6.</span><span class="sxs-lookup"><span data-stu-id="72f75-104">Determines whether the shape follows a parallel rotation, a perspective rotation, or an oblique rotation, as an integer from 0 to 6.</span></span> 
  
|<span data-ttu-id="72f75-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="72f75-105">**Value**</span></span>|<span data-ttu-id="72f75-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72f75-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="72f75-107">0</span><span class="sxs-lookup"><span data-stu-id="72f75-107">0</span></span>  <br/> |<span data-ttu-id="72f75-108">La forma no tiene ningún giro.</span><span class="sxs-lookup"><span data-stu-id="72f75-108">The shape does not have any rotation.</span></span>  <br/> |
|<span data-ttu-id="72f75-109">1</span><span class="sxs-lookup"><span data-stu-id="72f75-109">1</span></span>  <br/> |<span data-ttu-id="72f75-110">La forma tiene un giro en paralelo.</span><span class="sxs-lookup"><span data-stu-id="72f75-110">The shape has a parallel rotation.</span></span>  <br/> |
|<span data-ttu-id="72f75-111">2</span><span class="sxs-lookup"><span data-stu-id="72f75-111">2</span></span>  <br/> |<span data-ttu-id="72f75-112">La forma tiene una rotación en perspectiva.</span><span class="sxs-lookup"><span data-stu-id="72f75-112">The shape has a perspective rotation.</span></span>  <br/> |
|<span data-ttu-id="72f75-113">3</span><span class="sxs-lookup"><span data-stu-id="72f75-113">3</span></span>  <br/> |<span data-ttu-id="72f75-114">La forma tiene un giro oblicua hacia arriba e izquierdo superior.</span><span class="sxs-lookup"><span data-stu-id="72f75-114">The shape has a top left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="72f75-115">4</span><span class="sxs-lookup"><span data-stu-id="72f75-115">4</span></span>  <br/> |<span data-ttu-id="72f75-116">La forma tiene un giro oblicuo derecha superior.</span><span class="sxs-lookup"><span data-stu-id="72f75-116">The shape has a top right oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="72f75-117">5</span><span class="sxs-lookup"><span data-stu-id="72f75-117">5</span></span>  <br/> |<span data-ttu-id="72f75-118">La forma tiene un giro de oblicua hacia arriba e izquierda inferior.</span><span class="sxs-lookup"><span data-stu-id="72f75-118">The shape has a bottom left oblique rotation.</span></span>  <br/> |
|<span data-ttu-id="72f75-119">6</span><span class="sxs-lookup"><span data-stu-id="72f75-119">6</span></span>  <br/> |<span data-ttu-id="72f75-120">La forma tiene un inferior giro oblicua hacia la derecha.</span><span class="sxs-lookup"><span data-stu-id="72f75-120">The shape has a bottom right oblique rotation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72f75-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72f75-121">Remarks</span></span>

<span data-ttu-id="72f75-122">Para obtener una referencia a la celda **RotationType** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="72f75-122">To get a reference to the **RotationType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72f75-123">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="72f75-123">Cell name:</span></span>  <br/> |<span data-ttu-id="72f75-124">RotationType</span><span class="sxs-lookup"><span data-stu-id="72f75-124">RotationType</span></span>  <br/> |
   
<span data-ttu-id="72f75-125">Para obtener una referencia a la celda **RotationType** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="72f75-125">To get a reference to the **RotationType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72f75-126">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="72f75-126">Section index:</span></span>  <br/> |<span data-ttu-id="72f75-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="72f75-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="72f75-128">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="72f75-128">Row index:</span></span>  <br/> |<span data-ttu-id="72f75-129">**visRow3DRotationProperties**</span><span class="sxs-lookup"><span data-stu-id="72f75-129">**visRow3DRotationProperties**</span></span> <br/> |
|<span data-ttu-id="72f75-130">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="72f75-130">Cell index:</span></span>  <br/> |<span data-ttu-id="72f75-131">**visRotationType**</span><span class="sxs-lookup"><span data-stu-id="72f75-131">**visRotationType**</span></span> <br/> |
   

