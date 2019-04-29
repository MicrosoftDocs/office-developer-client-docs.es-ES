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
description: Devuelve la coordenada x (en el sistema local de coordenadas) del punto donde se cortan dos líneas.
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418277"
---
# <a name="intersectx-function"></a><span data-ttu-id="b71dd-103">Función INTERSECTX</span><span class="sxs-lookup"><span data-stu-id="b71dd-103">INTERSECTX Function</span></span>

<span data-ttu-id="b71dd-104">Devuelve la coordenada *x* (en el sistema local de coordenadas) del punto donde se cortan dos líneas.</span><span class="sxs-lookup"><span data-stu-id="b71dd-104">Returns the  *x*  -coordinate (in the local coordinate system) of the point where two lines intersect.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b71dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b71dd-105">Syntax</span></span>

<span data-ttu-id="b71dd-106">INTERSECTX (\* \* *x1* \* \*, \* \* *Y1* \* \*, \* \* *angle1* \* \*, \* \* *x2* \* \*, \* \* *Y2* \* \*, \* \* *angle2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b71dd-106">INTERSECTX(\*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *angle1* \*\*, \*\* *x2* \*\*, \*\* *y2* \*\*, \*\* *angle2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b71dd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b71dd-107">Parameters</span></span>

|<span data-ttu-id="b71dd-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b71dd-108">**Name**</span></span>|<span data-ttu-id="b71dd-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="b71dd-109">**Required/Optional**</span></span>|<span data-ttu-id="b71dd-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="b71dd-110">**Data Type**</span></span>|<span data-ttu-id="b71dd-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b71dd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b71dd-112">_1_</span><span class="sxs-lookup"><span data-stu-id="b71dd-112">_x1_</span></span> <br/> |<span data-ttu-id="b71dd-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b71dd-113">Required</span></span>  <br/> |<span data-ttu-id="b71dd-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="b71dd-114">**Number**</span></span> <br/> |<span data-ttu-id="b71dd-115">Coordenada _x_de un punto de la primera recta.</span><span class="sxs-lookup"><span data-stu-id="b71dd-115">The  _x_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="b71dd-116">_a1_</span><span class="sxs-lookup"><span data-stu-id="b71dd-116">_y1_</span></span> <br/> |<span data-ttu-id="b71dd-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b71dd-117">Required</span></span>  <br/> |<span data-ttu-id="b71dd-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="b71dd-118">**Number**</span></span> <br/> |<span data-ttu-id="b71dd-119">Coordenada _y_de un punto de la primera recta.</span><span class="sxs-lookup"><span data-stu-id="b71dd-119">The  _y_-coordinate of a point on the first line.</span></span>  <br/> |
| <span data-ttu-id="b71dd-120">_angle1_</span><span class="sxs-lookup"><span data-stu-id="b71dd-120">_angle1_</span></span> <br/> |<span data-ttu-id="b71dd-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b71dd-121">Required</span></span>  <br/> |<span data-ttu-id="b71dd-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="b71dd-122">**Number**</span></span> <br/> | <span data-ttu-id="b71dd-123">Valor de la celda Angle de la primera recta.</span><span class="sxs-lookup"><span data-stu-id="b71dd-123">The value of the Angle cell for the first line.</span></span>  <br/> |
| <span data-ttu-id="b71dd-124">_2x_</span><span class="sxs-lookup"><span data-stu-id="b71dd-124">_x2_</span></span> <br/> |<span data-ttu-id="b71dd-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b71dd-125">Required</span></span>  <br/> |<span data-ttu-id="b71dd-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="b71dd-126">**Number**</span></span> <br/> |<span data-ttu-id="b71dd-127">Coordenada _x_de un punto de la segunda recta.</span><span class="sxs-lookup"><span data-stu-id="b71dd-127">The  _x_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="b71dd-128">_Single_</span><span class="sxs-lookup"><span data-stu-id="b71dd-128">_y2_</span></span> <br/> |<span data-ttu-id="b71dd-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b71dd-129">Required</span></span>  <br/> |<span data-ttu-id="b71dd-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="b71dd-130">**Number**</span></span> <br/> |<span data-ttu-id="b71dd-131">Coordenada _y_de un punto de la segunda recta.</span><span class="sxs-lookup"><span data-stu-id="b71dd-131">The  _y_-coordinate of a point on the second line.</span></span>  <br/> |
| <span data-ttu-id="b71dd-132">_angle2_</span><span class="sxs-lookup"><span data-stu-id="b71dd-132">_angle2_</span></span> <br/> |<span data-ttu-id="b71dd-133">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b71dd-133">Required</span></span>  <br/> |<span data-ttu-id="b71dd-134">**Number**</span><span class="sxs-lookup"><span data-stu-id="b71dd-134">**Number**</span></span> <br/> |<span data-ttu-id="b71dd-135">Valor de la celda Angle de la segunda recta.</span><span class="sxs-lookup"><span data-stu-id="b71dd-135">The value of the Angle cell for the second line.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b71dd-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b71dd-136">Return value</span></span>

<span data-ttu-id="b71dd-137">Número</span><span class="sxs-lookup"><span data-stu-id="b71dd-137">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b71dd-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b71dd-138">Remarks</span></span>

<span data-ttu-id="b71dd-139">Cada línea se define como un punto (*x,y*) y un ángulo.</span><span class="sxs-lookup"><span data-stu-id="b71dd-139">Each line is defined as a point (*x,y*) and an angle.</span></span> 
  
<span data-ttu-id="b71dd-140">Microsoft Visio usa esta función en la celda PinX de una forma pegada a una guía girada.</span><span class="sxs-lookup"><span data-stu-id="b71dd-140">Microsoft Visio uses this function in the PinX cell of a shape glued to a rotated guide.</span></span> 
  
<span data-ttu-id="b71dd-141">Si las rectas no se cruzan, la función devuelve un error de división por cero (#DIV/0!), aunque Visio lo pasa por alto y restaura el último valor conocido para este punto.</span><span class="sxs-lookup"><span data-stu-id="b71dd-141">If the lines don't intersect, the function returns a divide-by-zero error (#DIV/0!), which Visio ignores, restoring the last known value for the point.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b71dd-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b71dd-142">Example</span></span>

<span data-ttu-id="b71dd-143">INTERSECTX (VertGuide! PinX, VertGuide! PinY, VertGuide! Angle, Guíahoriz! PinX, Guíahoriz! PinY, Guíahoriz! Respecto</span><span class="sxs-lookup"><span data-stu-id="b71dd-143">INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!Angle)</span></span> 
  
<span data-ttu-id="b71dd-144">Devuelve la coordenada *x* del punto de intersección de VertGuide y guíahoriz en las unidades de página.</span><span class="sxs-lookup"><span data-stu-id="b71dd-144">Returns the  *x*  -coordinate of the intersection point of VertGuide and HorzGuide in page units.</span></span> 
  

