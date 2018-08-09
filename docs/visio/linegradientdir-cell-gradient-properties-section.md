---
title: Celda LineGradientDir (sección Propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Determina la dirección de la línea de degradado. Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso.
ms.openlocfilehash: 6243d7a6b470db0915ba6fc462f05b72a9814f66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822466"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="844cd-104">Celda LineGradientDir (sección Propiedades de degradado)</span><span class="sxs-lookup"><span data-stu-id="844cd-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="844cd-105">Determina la dirección de la línea de degradado.</span><span class="sxs-lookup"><span data-stu-id="844cd-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="844cd-106">Un degradado puede ser lineal, radial, rectangular o seguir una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="844cd-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="844cd-107">Un degradado lineal es el degradado sólo que toma un valor de ángulo adicionales (según lo determinado por la celda **LineGradientDir** ).</span><span class="sxs-lookup"><span data-stu-id="844cd-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="844cd-108">Todas las demás direcciones de degradado tienen preestablecidas enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="844cd-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="844cd-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="844cd-109">**Value**</span></span>|<span data-ttu-id="844cd-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="844cd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="844cd-111">0</span><span class="sxs-lookup"><span data-stu-id="844cd-111">0</span></span>  <br/> |<span data-ttu-id="844cd-112">Degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="844cd-112">Linear gradient.</span></span> <span data-ttu-id="844cd-113">La celda **LineGradientAngle** determina la dirección del degradado.</span><span class="sxs-lookup"><span data-stu-id="844cd-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="844cd-114">1-7</span><span class="sxs-lookup"><span data-stu-id="844cd-114">1-7</span></span>  <br/> |<span data-ttu-id="844cd-115">Degradados radiales.</span><span class="sxs-lookup"><span data-stu-id="844cd-115">Radial gradients.</span></span> <span data-ttu-id="844cd-116">El degradado se extiende hacia el exterior en un círculo desde un punto central.</span><span class="sxs-lookup"><span data-stu-id="844cd-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="844cd-117">8-12</span><span class="sxs-lookup"><span data-stu-id="844cd-117">8-12</span></span>  <br/> |<span data-ttu-id="844cd-118">Degradados rectangulares.</span><span class="sxs-lookup"><span data-stu-id="844cd-118">Rectangular gradients.</span></span> <span data-ttu-id="844cd-119">El degradado se extiende como una línea direccional desde un origen con un desvanecimiento con forma rectangular.</span><span class="sxs-lookup"><span data-stu-id="844cd-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="844cd-120">13</span><span class="sxs-lookup"><span data-stu-id="844cd-120">13</span></span>  <br/> |<span data-ttu-id="844cd-121">Degradado de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="844cd-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="844cd-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="844cd-122">Remarks</span></span>

<span data-ttu-id="844cd-123">Para obtener una referencia a la celda **LineGradientDir** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="844cd-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="844cd-124">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="844cd-124">Cell name:</span></span>  <br/> | <span data-ttu-id="844cd-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="844cd-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="844cd-126">Para obtener una referencia a la celda **LineGradientDir** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="844cd-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="844cd-127">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="844cd-127">Section index:</span></span>  <br/> |<span data-ttu-id="844cd-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="844cd-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="844cd-129">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="844cd-129">Row index:</span></span>  <br/> |<span data-ttu-id="844cd-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="844cd-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="844cd-131">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="844cd-131">Cell index:</span></span>  <br/> |<span data-ttu-id="844cd-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="844cd-132">**visLineGradientDir**</span></span> <br/> |
   

