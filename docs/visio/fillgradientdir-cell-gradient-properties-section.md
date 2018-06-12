---
title: Celda FillGradientDir (sección de propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Determina la dirección del relleno degradado. Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso.
ms.openlocfilehash: 9b4226892e70fcffe7a78d109bd852e6d4f93838
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822130"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="5ef30-104">Celda FillGradientDir (sección de propiedades de degradado)</span><span class="sxs-lookup"><span data-stu-id="5ef30-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="5ef30-105">Determina la dirección del relleno degradado.</span><span class="sxs-lookup"><span data-stu-id="5ef30-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="5ef30-106">Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="5ef30-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5ef30-107">Un degradado lineal es el degradado sólo que toma un valor de ángulo adicionales (según lo determinado por la celda **FillGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="5ef30-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="5ef30-108">Todas las demás direcciones de degradado tienen preestablecidas enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="5ef30-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="5ef30-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5ef30-109">**Value**</span></span>|<span data-ttu-id="5ef30-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5ef30-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ef30-111">0</span><span class="sxs-lookup"><span data-stu-id="5ef30-111">0</span></span>  <br/> |<span data-ttu-id="5ef30-112">Degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="5ef30-112">Linear gradient.</span></span> <span data-ttu-id="5ef30-113">La celda **FillGradientAngle** determina la dirección del degradado.</span><span class="sxs-lookup"><span data-stu-id="5ef30-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="5ef30-114">1-7</span><span class="sxs-lookup"><span data-stu-id="5ef30-114">1-7</span></span>  <br/> |<span data-ttu-id="5ef30-115">Degradados radiales.</span><span class="sxs-lookup"><span data-stu-id="5ef30-115">Radial gradients.</span></span> <span data-ttu-id="5ef30-116">El degradado se extiende hacia el exterior en un círculo desde un punto central.</span><span class="sxs-lookup"><span data-stu-id="5ef30-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="5ef30-117">8-12</span><span class="sxs-lookup"><span data-stu-id="5ef30-117">8-12</span></span>  <br/> |<span data-ttu-id="5ef30-118">Degradados rectangulares.</span><span class="sxs-lookup"><span data-stu-id="5ef30-118">Rectangular gradients.</span></span> <span data-ttu-id="5ef30-119">El degradado se extiende como una línea direccional desde un origen con un desvanecimiento con forma rectangular.</span><span class="sxs-lookup"><span data-stu-id="5ef30-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="5ef30-120">13</span><span class="sxs-lookup"><span data-stu-id="5ef30-120">13</span></span>  <br/> |<span data-ttu-id="5ef30-121">Degradado de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="5ef30-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ef30-122">Notas</span><span class="sxs-lookup"><span data-stu-id="5ef30-122">Remarks</span></span>

<span data-ttu-id="5ef30-123">Para obtener una referencia a la celda **FillGradientDir** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="5ef30-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ef30-124">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="5ef30-124">Cell name:</span></span>  <br/> | <span data-ttu-id="5ef30-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="5ef30-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="5ef30-126">Para obtener una referencia a la celda **FillGradientDir** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5ef30-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ef30-127">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="5ef30-127">Section index:</span></span>  <br/> |<span data-ttu-id="5ef30-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5ef30-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5ef30-129">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="5ef30-129">Row index:</span></span>  <br/> |<span data-ttu-id="5ef30-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="5ef30-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="5ef30-131">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="5ef30-131">Cell index:</span></span>  <br/> |<span data-ttu-id="5ef30-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="5ef30-132">**visFillGradientDir**</span></span> <br/> |
   

