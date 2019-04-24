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
description: Devuelve el ángulo entre el vector representado por x, y y la dirección del eje x. El resultado es un número en la unidad de medida angular actual.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341485"
---
# <a name="atan2-function"></a><span data-ttu-id="7dc36-104">Función ATAN2</span><span class="sxs-lookup"><span data-stu-id="7dc36-104">ATAN2 Function</span></span>

<span data-ttu-id="7dc36-105">Devuelve el ángulo entre el vector representado por *x, y* y la dirección del eje *x* .</span><span class="sxs-lookup"><span data-stu-id="7dc36-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="7dc36-106">El resultado es un número en la unidad de medida angular actual.</span><span class="sxs-lookup"><span data-stu-id="7dc36-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7dc36-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7dc36-107">Syntax</span></span>

<span data-ttu-id="7dc36-108">ATAN2 (\* \* *y* \* \*, \* \* *x* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7dc36-108">ATAN2(\*\* *y* \*\*, \*\* *x* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7dc36-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7dc36-109">Parameters</span></span>

|<span data-ttu-id="7dc36-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="7dc36-110">**Name**</span></span>|<span data-ttu-id="7dc36-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="7dc36-111">**Required/Optional**</span></span>|<span data-ttu-id="7dc36-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="7dc36-112">**Data Type**</span></span>|<span data-ttu-id="7dc36-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7dc36-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7dc36-114">_y_</span><span class="sxs-lookup"><span data-stu-id="7dc36-114">_y_</span></span> <br/> |<span data-ttu-id="7dc36-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7dc36-115">Required</span></span>  <br/> |<span data-ttu-id="7dc36-116">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="7dc36-116">**Numeric**</span></span> <br/> |<span data-ttu-id="7dc36-117">Valor _y_del punto.</span><span class="sxs-lookup"><span data-stu-id="7dc36-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="7dc36-118">_x_</span><span class="sxs-lookup"><span data-stu-id="7dc36-118">_x_</span></span> <br/> |<span data-ttu-id="7dc36-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7dc36-119">Required</span></span>  <br/> |<span data-ttu-id="7dc36-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="7dc36-120">**Numeric**</span></span> <br/> |<span data-ttu-id="7dc36-121">Valor _x_del punto.</span><span class="sxs-lookup"><span data-stu-id="7dc36-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7dc36-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7dc36-122">Remarks</span></span>

<span data-ttu-id="7dc36-123">El arco tangente es el ángulo medido en sentido contrario a las agujas del reloj desde el eje *x* positivo hasta una línea que intersecta con el origen (0, 0) y el punto representado por *x* e *y* .</span><span class="sxs-lookup"><span data-stu-id="7dc36-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="7dc36-124">En Microsoft Office Visio, ATAN2(0;0) devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="7dc36-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="7dc36-125">Para hacer que los resultados de ATAN2 se den en una unidad de medida angular distinta, utilice la función DEG o RAD.</span><span class="sxs-lookup"><span data-stu-id="7dc36-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="7dc36-126">La función ATAN2 es la inversa de la función TAN.</span><span class="sxs-lookup"><span data-stu-id="7dc36-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="7dc36-127">La función ATAN2 devuelve el ángulo cuyo ángulo es igual a *y* dividido por *x* .</span><span class="sxs-lookup"><span data-stu-id="7dc36-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="7dc36-128">Si ATAN2 (*y, x*) representa un ángulo en un triángulo a la derecha, *y* es el "lado opuesto" y *x* es el "lado adyacente", por lo que la función se puede escribir como ATAN2 (opuesto a adyacente).</span><span class="sxs-lookup"><span data-stu-id="7dc36-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7dc36-129">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="7dc36-129">Example 1</span></span>

<span data-ttu-id="7dc36-130">ATAN2 (1,25, 2,25)</span><span class="sxs-lookup"><span data-stu-id="7dc36-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="7dc36-131">Devuelve 29,0456 grados.</span><span class="sxs-lookup"><span data-stu-id="7dc36-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7dc36-132">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="7dc36-132">Example 2</span></span>

<span data-ttu-id="7dc36-133">ATAN2 (1, RAIZ (3))</span><span class="sxs-lookup"><span data-stu-id="7dc36-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="7dc36-134">Devuelve 30 grados.</span><span class="sxs-lookup"><span data-stu-id="7dc36-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7dc36-135">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="7dc36-135">Example 3</span></span>

<span data-ttu-id="7dc36-136">ATAN2 (1, 1)</span><span class="sxs-lookup"><span data-stu-id="7dc36-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="7dc36-137">Devuelve 45 grados.</span><span class="sxs-lookup"><span data-stu-id="7dc36-137">Returns 45 deg</span></span>
  

