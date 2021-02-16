---
title: Celda FillGradientDir (Sección de propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Determina la dirección del degradado de relleno. Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406720"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="7962f-104">Celda FillGradientDir (Sección de propiedades de degradado)</span><span class="sxs-lookup"><span data-stu-id="7962f-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="7962f-105">Determina la dirección del degradado de relleno.</span><span class="sxs-lookup"><span data-stu-id="7962f-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="7962f-106">Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="7962f-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7962f-107">Un degradado lineal es el único degradado que toma un valor de ángulo adicional (determinado por **la celda FillGradientDir).**</span><span class="sxs-lookup"><span data-stu-id="7962f-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="7962f-108">Todas las demás direcciones de degradado tienen enumeraciones preestablecidas.</span><span class="sxs-lookup"><span data-stu-id="7962f-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="7962f-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7962f-109">**Value**</span></span>|<span data-ttu-id="7962f-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7962f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7962f-111">0</span><span class="sxs-lookup"><span data-stu-id="7962f-111">0</span></span>  <br/> |<span data-ttu-id="7962f-112">Degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="7962f-112">Linear gradient.</span></span> <span data-ttu-id="7962f-113">La **celda FillGradientAngle** determina la dirección del degradado.</span><span class="sxs-lookup"><span data-stu-id="7962f-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="7962f-114">1-7</span><span class="sxs-lookup"><span data-stu-id="7962f-114">1-7</span></span>  <br/> |<span data-ttu-id="7962f-115">Degradados radiales.</span><span class="sxs-lookup"><span data-stu-id="7962f-115">Radial gradients.</span></span> <span data-ttu-id="7962f-116">El degradado se extiende hacia afuera en un círculo desde un punto central.</span><span class="sxs-lookup"><span data-stu-id="7962f-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="7962f-117">8-12</span><span class="sxs-lookup"><span data-stu-id="7962f-117">8-12</span></span>  <br/> |<span data-ttu-id="7962f-118">Degradados rectangulares.</span><span class="sxs-lookup"><span data-stu-id="7962f-118">Rectangular gradients.</span></span> <span data-ttu-id="7962f-119">El degradado se extiende como una línea direccional desde un origen con un fundido de forma rectangular.</span><span class="sxs-lookup"><span data-stu-id="7962f-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="7962f-120">13 </span><span class="sxs-lookup"><span data-stu-id="7962f-120">13</span></span>  <br/> |<span data-ttu-id="7962f-121">Degradado de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="7962f-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7962f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7962f-122">Remarks</span></span>

<span data-ttu-id="7962f-123">Para obtener una referencia a la celda **FillGradientDir** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="7962f-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7962f-124">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="7962f-124">Cell name:</span></span>  <br/> | <span data-ttu-id="7962f-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="7962f-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="7962f-126">Para obtener una referencia desde un programa a la celda **FillGradientDir** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7962f-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7962f-127">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="7962f-127">Section index:</span></span>  <br/> |<span data-ttu-id="7962f-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7962f-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7962f-129">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="7962f-129">Row index:</span></span>  <br/> |<span data-ttu-id="7962f-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="7962f-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="7962f-131">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="7962f-131">Cell index:</span></span>  <br/> |<span data-ttu-id="7962f-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="7962f-132">**visFillGradientDir**</span></span> <br/> |
   

