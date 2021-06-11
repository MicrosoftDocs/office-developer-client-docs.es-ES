---
title: Celda CompoundType (sección Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Determina el tipo compuesto de la línea de una forma.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407175"
---
# <a name="compoundtype-cell-line-format-section"></a><span data-ttu-id="11e09-103">Celda CompoundType (sección Line Format)</span><span class="sxs-lookup"><span data-stu-id="11e09-103">CompoundType Cell (Line Format Section)</span></span>

<span data-ttu-id="11e09-104">Determina el tipo compuesto de la línea de una forma.</span><span class="sxs-lookup"><span data-stu-id="11e09-104">Determines the compound type of the line of a shape.</span></span> 
  
|<span data-ttu-id="11e09-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="11e09-105">**Value**</span></span>|<span data-ttu-id="11e09-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="11e09-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="11e09-107">0</span><span class="sxs-lookup"><span data-stu-id="11e09-107">0</span></span>  <br/> |<span data-ttu-id="11e09-108">Sencillo</span><span class="sxs-lookup"><span data-stu-id="11e09-108">Simple</span></span>  <br/> |
|<span data-ttu-id="11e09-109">1</span><span class="sxs-lookup"><span data-stu-id="11e09-109">1</span></span>  <br/> |<span data-ttu-id="11e09-110">Doble</span><span class="sxs-lookup"><span data-stu-id="11e09-110">Double</span></span>  <br/> |
|<span data-ttu-id="11e09-111">2</span><span class="sxs-lookup"><span data-stu-id="11e09-111">2</span></span>  <br/> |<span data-ttu-id="11e09-112">Grosor fino</span><span class="sxs-lookup"><span data-stu-id="11e09-112">Thick thin</span></span>  <br/> |
|<span data-ttu-id="11e09-113">3</span><span class="sxs-lookup"><span data-stu-id="11e09-113">3</span></span>  <br/> |<span data-ttu-id="11e09-114">Grosor fino</span><span class="sxs-lookup"><span data-stu-id="11e09-114">Thin thick</span></span>  <br/> |
|<span data-ttu-id="11e09-115">4 </span><span class="sxs-lookup"><span data-stu-id="11e09-115">4</span></span>  <br/> |<span data-ttu-id="11e09-116">Triple</span><span class="sxs-lookup"><span data-stu-id="11e09-116">Triple</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11e09-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11e09-117">Remarks</span></span>

<span data-ttu-id="11e09-118">Para obtener una referencia a la **celda CompoundType** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la **propiedad CellsU,** use:</span><span class="sxs-lookup"><span data-stu-id="11e09-118">To get a reference to the **CompoundType** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11e09-119">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="11e09-119">Cell name:</span></span>  <br/> | <span data-ttu-id="11e09-120">CompoundType</span><span class="sxs-lookup"><span data-stu-id="11e09-120">CompoundType</span></span>  <br/> |
   
<span data-ttu-id="11e09-121">Para obtener una referencia desde un programa a la **celda CompoundType** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="11e09-121">To get a reference to the **CompoundType** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11e09-122">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="11e09-122">Section index:</span></span>  <br/> |<span data-ttu-id="11e09-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="11e09-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="11e09-124">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="11e09-124">Row index:</span></span>  <br/> |<span data-ttu-id="11e09-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="11e09-125">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="11e09-126">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="11e09-126">Cell index:</span></span>  <br/> |<span data-ttu-id="11e09-127">**visCompoundType**</span><span class="sxs-lookup"><span data-stu-id="11e09-127">**visCompoundType**</span></span> <br/> |
   

