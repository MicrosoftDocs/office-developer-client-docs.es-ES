---
title: INTERSECTY (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Devuelve la y-coordenada (en el sistema de coordenadas local) del punto donde se cortan dos líneas.
ms.openlocfilehash: c3c0e9afef317ed4c647f1d236c4c3a29c6cdaa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822345"
---
# <a name="intersecty-function"></a><span data-ttu-id="26b33-103">Función INTERSECTY</span><span class="sxs-lookup"><span data-stu-id="26b33-103">INTERSECTY Function</span></span>

<span data-ttu-id="26b33-104">Devuelve la *y* -coordenada (en el sistema de coordenadas local) del punto donde se cortan dos líneas.</span><span class="sxs-lookup"><span data-stu-id="26b33-104">Returns the  *y*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="26b33-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26b33-105">Syntax</span></span>

<span data-ttu-id="26b33-106">INTERSECTX (** *x1* **, ** *y1* **, ** *ángulo1* **, ** *x2* **, ** *y2* **, ** *ángulo2* **)</span><span class="sxs-lookup"><span data-stu-id="26b33-106">INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="26b33-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26b33-107">Parameters</span></span>

|<span data-ttu-id="26b33-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="26b33-108">**Name**</span></span>|<span data-ttu-id="26b33-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="26b33-109">**Required/Optional**</span></span>|<span data-ttu-id="26b33-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="26b33-110">**Data Type**</span></span>|<span data-ttu-id="26b33-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26b33-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="26b33-112">_X1_</span><span class="sxs-lookup"><span data-stu-id="26b33-112">_x1_</span></span> <br/> |<span data-ttu-id="26b33-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="26b33-113">Required</span></span>  <br/> |<span data-ttu-id="26b33-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="26b33-114">**Number**</span></span> <br/> |<span data-ttu-id="26b33-115">La _x_-coordenadas de un punto de la primera línea.</span><span class="sxs-lookup"><span data-stu-id="26b33-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="26b33-116">_Y1_</span><span class="sxs-lookup"><span data-stu-id="26b33-116">_y1_</span></span> <br/> |<span data-ttu-id="26b33-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="26b33-117">Required</span></span>  <br/> |<span data-ttu-id="26b33-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="26b33-118">**Number**</span></span> <br/> |<span data-ttu-id="26b33-119">La _y_-coordenadas de un punto de la primera línea.</span><span class="sxs-lookup"><span data-stu-id="26b33-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="26b33-120">_ángulo1_</span><span class="sxs-lookup"><span data-stu-id="26b33-120">_angle1_</span></span> <br/> |<span data-ttu-id="26b33-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="26b33-121">Required</span></span>  <br/> |<span data-ttu-id="26b33-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="26b33-122">**Number**</span></span> <br/> | <span data-ttu-id="26b33-123">Valor de la celda Angle de la primera recta.</span><span class="sxs-lookup"><span data-stu-id="26b33-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="26b33-124">_X2_</span><span class="sxs-lookup"><span data-stu-id="26b33-124">_x2_</span></span> <br/> |<span data-ttu-id="26b33-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="26b33-125">Required</span></span>  <br/> |<span data-ttu-id="26b33-126">**Número**</span><span class="sxs-lookup"><span data-stu-id="26b33-126">**Number**</span></span> <br/> |<span data-ttu-id="26b33-127">La _x_-coordenadas de un punto de la segunda recta.</span><span class="sxs-lookup"><span data-stu-id="26b33-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="26b33-128">_y2_</span><span class="sxs-lookup"><span data-stu-id="26b33-128">_y2_</span></span> <br/> |<span data-ttu-id="26b33-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="26b33-129">Required</span></span>  <br/> |<span data-ttu-id="26b33-130">**Número**</span><span class="sxs-lookup"><span data-stu-id="26b33-130">**Number**</span></span> <br/> |<span data-ttu-id="26b33-131">La _y_-coordenadas de un punto de la segunda recta.</span><span class="sxs-lookup"><span data-stu-id="26b33-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="26b33-132">_ángulo2_</span><span class="sxs-lookup"><span data-stu-id="26b33-132">_angle2_</span></span> <br/> |<span data-ttu-id="26b33-133">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="26b33-133">Required</span></span>  <br/> |<span data-ttu-id="26b33-134">**Número**</span><span class="sxs-lookup"><span data-stu-id="26b33-134">**Number**</span></span> <br/> |<span data-ttu-id="26b33-135">Valor de la celda Angle de la segunda recta.</span><span class="sxs-lookup"><span data-stu-id="26b33-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="26b33-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26b33-136">Return value</span></span>

<span data-ttu-id="26b33-137">Number</span><span class="sxs-lookup"><span data-stu-id="26b33-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26b33-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26b33-138">Remarks</span></span>

<span data-ttu-id="26b33-139">Cada línea se define como un punto (*x,y*) y un ángulo.</span><span class="sxs-lookup"><span data-stu-id="26b33-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="26b33-140">Microsoft Visio usa esta función en la celda PinY de una forma pegada a una guía girada.</span><span class="sxs-lookup"><span data-stu-id="26b33-140">Microsoft Visio uses this function in the PinY cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="26b33-141">Si las rectas no se cruzan, la función devuelve un error de división por cero (#DIV/0!), aunque Visio lo pasa por alto y restaura el último valor conocido para este punto.</span><span class="sxs-lookup"><span data-stu-id="26b33-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="26b33-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="26b33-142">Example</span></span>

<span data-ttu-id="26b33-143">¡INTERSECTY (VertGuide! ¡PinX, VertGuide! PinY, VertGuide! ¡GuíaVertical! ¡PinX, GuíaHoriz! PinY, GuíaHoriz! Ángulo)</span><span class="sxs-lookup"><span data-stu-id="26b33-143">INTERSECTY(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="26b33-144">Devuelve la *y* -coordenadas del punto donde se cortan GuíaVertical y GuíaHoriz en unidades de página.</span><span class="sxs-lookup"><span data-stu-id="26b33-144">Returns the  *y*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

