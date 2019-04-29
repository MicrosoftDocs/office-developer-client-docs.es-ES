---
title: Celda FillGradientDir (sección Propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Determina la dirección del degradado de relleno. Un degradado puede ser lineal, radial, rectangular o seguir una trayectoria.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406720"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="4fd07-104">Celda FillGradientDir (sección Propiedades de degradado)</span><span class="sxs-lookup"><span data-stu-id="4fd07-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="4fd07-105">Determina la dirección del degradado de relleno.</span><span class="sxs-lookup"><span data-stu-id="4fd07-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="4fd07-106">Un degradado puede ser lineal, radial, rectangular o seguir una trayectoria.</span><span class="sxs-lookup"><span data-stu-id="4fd07-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4fd07-107">Un degradado lineal es el único degradado que toma un valor de ángulo adicional (según se determina por la celda **FillGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="4fd07-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="4fd07-108">Todas las demás direcciones de degradado tienen enumeraciones preestablecidas.</span><span class="sxs-lookup"><span data-stu-id="4fd07-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="4fd07-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4fd07-109">**Value**</span></span>|<span data-ttu-id="4fd07-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4fd07-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4fd07-111">comprendi</span><span class="sxs-lookup"><span data-stu-id="4fd07-111">0</span></span>  <br/> |<span data-ttu-id="4fd07-112">Degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="4fd07-112">Linear gradient.</span></span> <span data-ttu-id="4fd07-113">La celda **FillGradientAngle** determina la dirección del degradado.</span><span class="sxs-lookup"><span data-stu-id="4fd07-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="4fd07-114">1-7</span><span class="sxs-lookup"><span data-stu-id="4fd07-114">1-7</span></span>  <br/> |<span data-ttu-id="4fd07-115">Degradados radiales.</span><span class="sxs-lookup"><span data-stu-id="4fd07-115">Radial gradients.</span></span> <span data-ttu-id="4fd07-116">El degradado se extiende hacia afuera en un círculo desde un punto central.</span><span class="sxs-lookup"><span data-stu-id="4fd07-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="4fd07-117">8-12</span><span class="sxs-lookup"><span data-stu-id="4fd07-117">8-12</span></span>  <br/> |<span data-ttu-id="4fd07-118">Degradados rectangulares.</span><span class="sxs-lookup"><span data-stu-id="4fd07-118">Rectangular gradients.</span></span> <span data-ttu-id="4fd07-119">El degradado se extiende como una línea direccional desde un origen con una atenuación de forma rectangular.</span><span class="sxs-lookup"><span data-stu-id="4fd07-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="4fd07-120">13 </span><span class="sxs-lookup"><span data-stu-id="4fd07-120">13</span></span>  <br/> |<span data-ttu-id="4fd07-121">Degradado de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="4fd07-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fd07-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4fd07-122">Remarks</span></span>

<span data-ttu-id="4fd07-123">Para obtener una referencia a la celda **FillGradientDir** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="4fd07-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4fd07-124">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4fd07-124">Cell name:</span></span>  <br/> | <span data-ttu-id="4fd07-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="4fd07-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="4fd07-126">Para obtener una referencia desde un programa a la celda **FillGradientDir** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4fd07-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4fd07-127">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4fd07-127">Section index:</span></span>  <br/> |<span data-ttu-id="4fd07-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4fd07-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4fd07-129">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4fd07-129">Row index:</span></span>  <br/> |<span data-ttu-id="4fd07-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="4fd07-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="4fd07-131">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4fd07-131">Cell index:</span></span>  <br/> |<span data-ttu-id="4fd07-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="4fd07-132">**visFillGradientDir**</span></span> <br/> |
   

