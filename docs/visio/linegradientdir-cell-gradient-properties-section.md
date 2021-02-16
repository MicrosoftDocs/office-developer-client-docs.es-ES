---
title: Celda LineGradientDir (Sección de propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Determina la dirección del degradado de línea. Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417990"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="84f66-104">Celda LineGradientDir (Sección de propiedades de degradado)</span><span class="sxs-lookup"><span data-stu-id="84f66-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="84f66-105">Determina la dirección del degradado de línea.</span><span class="sxs-lookup"><span data-stu-id="84f66-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="84f66-106">Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="84f66-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="84f66-107">Un degradado lineal es el único degradado que toma un valor de ángulo adicional (determinado por **la celda LineGradientDir).**</span><span class="sxs-lookup"><span data-stu-id="84f66-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="84f66-108">Todas las demás direcciones de degradado tienen enumeraciones preestablecidas.</span><span class="sxs-lookup"><span data-stu-id="84f66-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="84f66-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="84f66-109">**Value**</span></span>|<span data-ttu-id="84f66-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="84f66-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="84f66-111">0</span><span class="sxs-lookup"><span data-stu-id="84f66-111">0</span></span>  <br/> |<span data-ttu-id="84f66-112">Degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="84f66-112">Linear gradient.</span></span> <span data-ttu-id="84f66-113">La **celda LineGradientAngle** determina la dirección del degradado.</span><span class="sxs-lookup"><span data-stu-id="84f66-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="84f66-114">1-7</span><span class="sxs-lookup"><span data-stu-id="84f66-114">1-7</span></span>  <br/> |<span data-ttu-id="84f66-115">Degradados radiales.</span><span class="sxs-lookup"><span data-stu-id="84f66-115">Radial gradients.</span></span> <span data-ttu-id="84f66-116">El degradado se extiende hacia afuera en un círculo desde un punto central.</span><span class="sxs-lookup"><span data-stu-id="84f66-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="84f66-117">8-12</span><span class="sxs-lookup"><span data-stu-id="84f66-117">8-12</span></span>  <br/> |<span data-ttu-id="84f66-118">Degradados rectangulares.</span><span class="sxs-lookup"><span data-stu-id="84f66-118">Rectangular gradients.</span></span> <span data-ttu-id="84f66-119">El degradado se extiende como una línea direccional desde un origen con un fundido de forma rectangular.</span><span class="sxs-lookup"><span data-stu-id="84f66-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="84f66-120">13 </span><span class="sxs-lookup"><span data-stu-id="84f66-120">13</span></span>  <br/> |<span data-ttu-id="84f66-121">Degradado de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="84f66-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84f66-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84f66-122">Remarks</span></span>

<span data-ttu-id="84f66-123">Para obtener una referencia a la celda **LineGradientDir** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="84f66-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="84f66-124">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="84f66-124">Cell name:</span></span>  <br/> | <span data-ttu-id="84f66-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="84f66-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="84f66-126">Para obtener una referencia desde un programa a la **celda LineGradientDir** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="84f66-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="84f66-127">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="84f66-127">Section index:</span></span>  <br/> |<span data-ttu-id="84f66-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="84f66-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="84f66-129">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="84f66-129">Row index:</span></span>  <br/> |<span data-ttu-id="84f66-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="84f66-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="84f66-131">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="84f66-131">Cell index:</span></span>  <br/> |<span data-ttu-id="84f66-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="84f66-132">**visLineGradientDir**</span></span> <br/> |
   

