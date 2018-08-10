---
title: ATAN2 (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: Devuelve el ángulo entre el vector representado por x, y y la dirección de la x-eje. El resultado es un número en la unidad actual de medida para los ángulos.
ms.openlocfilehash: dfd62ce628a3a46ff14b3ffc3f07074a39c66e14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821526"
---
# <a name="atan2-function"></a><span data-ttu-id="0cb86-104">Función ATAN2</span><span class="sxs-lookup"><span data-stu-id="0cb86-104">ATAN2 Function</span></span>

<span data-ttu-id="0cb86-105">Devuelve el ángulo entre el vector representado por *x, y* y la dirección de la *x* -eje.</span><span class="sxs-lookup"><span data-stu-id="0cb86-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="0cb86-106">El resultado es un número en la unidad actual de medida para los ángulos.</span><span class="sxs-lookup"><span data-stu-id="0cb86-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0cb86-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cb86-107">Syntax</span></span>

<span data-ttu-id="0cb86-108">ATAN2 (** *y* **, ** *x* **)</span><span class="sxs-lookup"><span data-stu-id="0cb86-108">ATAN2(** *y* **, ** *x* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0cb86-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cb86-109">Parameters</span></span>

|<span data-ttu-id="0cb86-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="0cb86-110">**Name**</span></span>|<span data-ttu-id="0cb86-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="0cb86-111">**Required/Optional**</span></span>|<span data-ttu-id="0cb86-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0cb86-112">**Data Type**</span></span>|<span data-ttu-id="0cb86-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0cb86-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0cb86-114">_y_</span><span class="sxs-lookup"><span data-stu-id="0cb86-114">_y_</span></span> <br/> |<span data-ttu-id="0cb86-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0cb86-115">Required</span></span>  <br/> |<span data-ttu-id="0cb86-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="0cb86-116">**Numeric**</span></span> <br/> |<span data-ttu-id="0cb86-117">La _y_-valor del punto.</span><span class="sxs-lookup"><span data-stu-id="0cb86-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="0cb86-118">_x_</span><span class="sxs-lookup"><span data-stu-id="0cb86-118">_x_</span></span> <br/> |<span data-ttu-id="0cb86-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0cb86-119">Required</span></span>  <br/> |<span data-ttu-id="0cb86-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="0cb86-120">**Numeric**</span></span> <br/> |<span data-ttu-id="0cb86-121">La _x_-valor del punto.</span><span class="sxs-lookup"><span data-stu-id="0cb86-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cb86-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0cb86-122">Remarks</span></span>

<span data-ttu-id="0cb86-123">El arco tangente es el ángulo ascendente medido desde el positivo *x* -eje a una línea que cruza el origen (0,0) y el punto representado por *x* e *y* .</span><span class="sxs-lookup"><span data-stu-id="0cb86-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="0cb86-124">En Microsoft Visio, ATAN2(0,0) devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="0cb86-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="0cb86-125">Para forzar el resultado de ATAN2 en una medida angular distinta, utilice la función DEG o RAD.</span><span class="sxs-lookup"><span data-stu-id="0cb86-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="0cb86-126">La función ATAN2 es la inversa de la función TAN.</span><span class="sxs-lookup"><span data-stu-id="0cb86-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="0cb86-127">La función ATAN2 Devuelve el ángulo cuya tangente es igual a *y* dividido entre *x* .</span><span class="sxs-lookup"><span data-stu-id="0cb86-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="0cb86-128">Si ATAN2 (*y, x*) representa un ángulo en un triángulo rectángulo, *y* es el "lado opuesto" y *x* es el "lado adyacente", por lo que la función podría escribirse como ATAN2(opposite,adjacent).</span><span class="sxs-lookup"><span data-stu-id="0cb86-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="0cb86-129">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="0cb86-129">Example 1</span></span>

<span data-ttu-id="0cb86-130">ATAN2(1.25,2.25)</span><span class="sxs-lookup"><span data-stu-id="0cb86-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="0cb86-131">Devuelve 29,0456 grados.</span><span class="sxs-lookup"><span data-stu-id="0cb86-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0cb86-132">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="0cb86-132">Example 2</span></span>

<span data-ttu-id="0cb86-133">ATAN2(1;SQRT(3))</span><span class="sxs-lookup"><span data-stu-id="0cb86-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="0cb86-134">Devuelve 30 grados.</span><span class="sxs-lookup"><span data-stu-id="0cb86-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0cb86-135">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="0cb86-135">Example 3</span></span>

<span data-ttu-id="0cb86-136">ATAN2(1;1)</span><span class="sxs-lookup"><span data-stu-id="0cb86-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="0cb86-137">Devuelve 45 grados.</span><span class="sxs-lookup"><span data-stu-id="0cb86-137">Returns 45 deg</span></span>
  

