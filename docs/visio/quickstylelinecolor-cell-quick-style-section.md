---
title: Celda QuickStyleLineColor (sección Estilo rápido)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: Determina qué color de tema usa la línea de una forma, como un entero de 0 a 7.
ms.openlocfilehash: 010b943f2266b1e0ee192e5f1341d73851d176fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437046"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a><span data-ttu-id="94032-103">Celda QuickStyleLineColor (sección Estilo rápido)</span><span class="sxs-lookup"><span data-stu-id="94032-103">QuickStyleLineColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="94032-104">Determina qué color de tema usa la línea de una forma, como un entero de 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="94032-104">Determines which theme color that a shape's line uses, as an integer from 0 to 7.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94032-105">Valor</span><span class="sxs-lookup"><span data-stu-id="94032-105">Value</span></span>  <br/> |<span data-ttu-id="94032-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="94032-106">Description</span></span>  <br/> |
|<span data-ttu-id="94032-107">0</span><span class="sxs-lookup"><span data-stu-id="94032-107">0</span></span>  <br/> |<span data-ttu-id="94032-108">El color de línea de forma hereda del color del tema Oscuro.</span><span class="sxs-lookup"><span data-stu-id="94032-108">The shape line color inherits from the Dark theme color.</span></span>  <br/> |
|<span data-ttu-id="94032-109">1</span><span class="sxs-lookup"><span data-stu-id="94032-109">1</span></span>  <br/> |<span data-ttu-id="94032-110">El color de línea de forma hereda del color del tema Light.</span><span class="sxs-lookup"><span data-stu-id="94032-110">The shape line color inherits from the Light theme color.</span></span>  <br/> |
|<span data-ttu-id="94032-111">2</span><span class="sxs-lookup"><span data-stu-id="94032-111">2</span></span>  <br/> |<span data-ttu-id="94032-112">El color de la línea de formas se hereda del color del tema Énfal 1</span><span class="sxs-lookup"><span data-stu-id="94032-112">The shape line color inherits from the Accent 1 theme color</span></span>  <br/> |
|<span data-ttu-id="94032-113">3</span><span class="sxs-lookup"><span data-stu-id="94032-113">3</span></span>  <br/> |<span data-ttu-id="94032-114">El color de la línea de forma se hereda del color del tema Énfal 2</span><span class="sxs-lookup"><span data-stu-id="94032-114">The shape line color inherits from the Accent 2 theme color</span></span>  <br/> |
|<span data-ttu-id="94032-115">4 </span><span class="sxs-lookup"><span data-stu-id="94032-115">4</span></span>  <br/> |<span data-ttu-id="94032-116">El color de la línea de forma se hereda del color del tema Énfal 3</span><span class="sxs-lookup"><span data-stu-id="94032-116">The shape line color inherits from the Accent 3 theme color</span></span>  <br/> |
|<span data-ttu-id="94032-117">5 </span><span class="sxs-lookup"><span data-stu-id="94032-117">5</span></span>  <br/> |<span data-ttu-id="94032-118">El color de línea de forma se hereda del color del tema Énfénf 4</span><span class="sxs-lookup"><span data-stu-id="94032-118">The shape line color inherits from the Accent 4 theme color</span></span>  <br/> |
|<span data-ttu-id="94032-119">6 </span><span class="sxs-lookup"><span data-stu-id="94032-119">6</span></span>  <br/> |<span data-ttu-id="94032-120">El color de línea de forma se hereda del color del tema Énfal 5</span><span class="sxs-lookup"><span data-stu-id="94032-120">The shape line color inherits from the Accent 5 theme color</span></span>  <br/> |
|<span data-ttu-id="94032-121">7 </span><span class="sxs-lookup"><span data-stu-id="94032-121">7</span></span>  <br/> |<span data-ttu-id="94032-122">El color de línea de forma se hereda del color del tema Énfénf 6</span><span class="sxs-lookup"><span data-stu-id="94032-122">The shape line color inherits from the Accent 6 theme color</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94032-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94032-123">Remarks</span></span>

<span data-ttu-id="94032-124">Para obtener una referencia a la **celda QuickStyleLineColor** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="94032-124">To get a reference to the **QuickStyleLineColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94032-125">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="94032-125">Cell name:</span></span>  <br/> | <span data-ttu-id="94032-126">QuickStyleLineColor</span><span class="sxs-lookup"><span data-stu-id="94032-126">QuickStyleLineColor</span></span>  <br/> |
   
<span data-ttu-id="94032-127">Para obtener una referencia desde un programa a la **celda QuickStyleLineColor** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="94032-127">To get a reference to the **QuickStyleLineColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="94032-128">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="94032-128">Section index:</span></span>  <br/> |<span data-ttu-id="94032-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="94032-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="94032-130">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="94032-130">Row index:</span></span>  <br/> |<span data-ttu-id="94032-131">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="94032-131">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="94032-132">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="94032-132">Cell index:</span></span>  <br/> |<span data-ttu-id="94032-133">**visQuickStyleLineColor**</span><span class="sxs-lookup"><span data-stu-id="94032-133">**visQuickStyleLineColor**</span></span> <br/> |
   

