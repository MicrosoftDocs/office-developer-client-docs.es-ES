---
title: INTERSECTX (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
localization_priority: Normal
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: Devuelve la x-coordenada (en el sistema de coordenadas local) del punto donde se cortan dos líneas.
ms.openlocfilehash: ea5a08f25f3e45dab3fe3fd83b74cf9a7541b6e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822342"
---
# <a name="intersectx-function"></a><span data-ttu-id="f1ac8-103">Función INTERSECTX</span><span class="sxs-lookup"><span data-stu-id="f1ac8-103">INTERSECTX Function</span></span>

<span data-ttu-id="f1ac8-104">Devuelve la *x* -coordenada (en el sistema de coordenadas local) del punto donde se cortan dos líneas.</span><span class="sxs-lookup"><span data-stu-id="f1ac8-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f1ac8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1ac8-105">Syntax</span></span>

<span data-ttu-id="f1ac8-106">INTERSECTX (** *x1* **, ** *y1* **, ** *ángulo1* **, ** *x2* **, ** *y2* **, ** *ángulo2* **)</span><span class="sxs-lookup"><span data-stu-id="f1ac8-106">INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f1ac8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1ac8-107">Parameters</span></span>

|<span data-ttu-id="f1ac8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f1ac8-108">**Name**</span></span>|<span data-ttu-id="f1ac8-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="f1ac8-109">**Required/Optional**</span></span>|<span data-ttu-id="f1ac8-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="f1ac8-110">**Data Type**</span></span>|<span data-ttu-id="f1ac8-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1ac8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f1ac8-112">_X1_</span><span class="sxs-lookup"><span data-stu-id="f1ac8-112">_x1_</span></span> <br/> |<span data-ttu-id="f1ac8-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f1ac8-113">Required</span></span>  <br/> |<span data-ttu-id="f1ac8-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="f1ac8-114">**Number**</span></span> <br/> |<span data-ttu-id="f1ac8-115">La _x_-coordenadas de un punto de la primera línea.</span><span class="sxs-lookup"><span data-stu-id="f1ac8-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="f1ac8-116">_Y1_</span><span class="sxs-lookup"><span data-stu-id="f1ac8-116">_y1_</span></span> <br/> |<span data-ttu-id="f1ac8-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f1ac8-117">Required</span></span>  <br/> |<span data-ttu-id="f1ac8-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="f1ac8-118">**Number**</span></span> <br/> |<span data-ttu-id="f1ac8-119">La _y_-coordenadas de un punto de la primera línea.</span><span class="sxs-lookup"><span data-stu-id="f1ac8-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="f1ac8-120">_ángulo1_</span><span class="sxs-lookup"><span data-stu-id="f1ac8-120">_angle1_</span></span> <br/> |<span data-ttu-id="f1ac8-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f1ac8-121">Required</span></span>  <br/> |<span data-ttu-id="f1ac8-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="f1ac8-122">**Number**</span></span> <br/> | <span data-ttu-id="f1ac8-123">Valor de la celda Angle de la primera recta.</span><span class="sxs-lookup"><span data-stu-id="f1ac8-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="f1ac8-124">_X2_</span><span class="sxs-lookup"><span data-stu-id="f1ac8-124">_x2_</span></span> <br/> |<span data-ttu-id="f1ac8-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f1ac8-125">Required</span></span>  <br/> |<span data-ttu-id="f1ac8-126">**Número**</span><span class="sxs-lookup"><span data-stu-id="f1ac8-126">**Number**</span></span> <br/> |<span data-ttu-id="f1ac8-127">La _x_-coordenadas de un punto de la segunda recta.</span><span class="sxs-lookup"><span data-stu-id="f1ac8-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="f1ac8-128">_y2_</span><span class="sxs-lookup"><span data-stu-id="f1ac8-128">_y2_</span></span> <br/> |<span data-ttu-id="f1ac8-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f1ac8-129">Required</span></span>  <br/> |<span data-ttu-id="f1ac8-130">**Número**</span><span class="sxs-lookup"><span data-stu-id="f1ac8-130">**Number**</span></span> <br/> |<span data-ttu-id="f1ac8-131">La _y_-coordenadas de un punto de la segunda recta.</span><span class="sxs-lookup"><span data-stu-id="f1ac8-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="f1ac8-132">_ángulo2_</span><span class="sxs-lookup"><span data-stu-id="f1ac8-132">_angle2_</span></span> <br/> |<span data-ttu-id="f1ac8-133">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f1ac8-133">Required</span></span>  <br/> |<span data-ttu-id="f1ac8-134">**Número**</span><span class="sxs-lookup"><span data-stu-id="f1ac8-134">**Number**</span></span> <br/> |<span data-ttu-id="f1ac8-135">Valor de la celda Angle de la segunda recta.</span><span class="sxs-lookup"><span data-stu-id="f1ac8-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f1ac8-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1ac8-136">Return value</span></span>

<span data-ttu-id="f1ac8-137">Number</span><span class="sxs-lookup"><span data-stu-id="f1ac8-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1ac8-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1ac8-138">Remarks</span></span>

<span data-ttu-id="f1ac8-139">Cada línea se define como un punto (*x,y*) y un ángulo.</span><span class="sxs-lookup"><span data-stu-id="f1ac8-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="f1ac8-140">Microsoft Visio usa esta función en la celda PinX de una forma pegada a una guía girada.</span><span class="sxs-lookup"><span data-stu-id="f1ac8-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="f1ac8-141">Si las rectas no se cruzan, la función devuelve un error de división por cero (#DIV/0!), aunque Visio lo pasa por alto y restaura el último valor conocido para este punto.</span><span class="sxs-lookup"><span data-stu-id="f1ac8-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f1ac8-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1ac8-142">Example</span></span>

<span data-ttu-id="f1ac8-143">¡INTERSECTX (VertGuide! ¡PinX, VertGuide! PinY, VertGuide! ¡GuíaVertical! ¡PinX, GuíaHoriz! PinY, GuíaHoriz! Ángulo)</span><span class="sxs-lookup"><span data-stu-id="f1ac8-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="f1ac8-144">Devuelve la *x* -coordenadas del punto donde se cortan GuíaVertical y GuíaHoriz en unidades de página.</span><span class="sxs-lookup"><span data-stu-id="f1ac8-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

