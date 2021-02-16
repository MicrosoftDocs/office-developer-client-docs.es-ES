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
description: Devuelve el ángulo entre el vector representado por x,y y la dirección del eje X. El resultado es un número en la unidad de medida angular actual.
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436485"
---
# <a name="atan2-function"></a><span data-ttu-id="4565d-104">Función ATAN2</span><span class="sxs-lookup"><span data-stu-id="4565d-104">ATAN2 Function</span></span>

<span data-ttu-id="4565d-105">Devuelve el ángulo entre el vector representado por *x,y* y la dirección del *eje X.*</span><span class="sxs-lookup"><span data-stu-id="4565d-105">Returns the angle between the vector represented by  *x,y*  and the direction of the  *x*  -axis.</span></span> <span data-ttu-id="4565d-106">El resultado es un número en la unidad de medida angular actual.</span><span class="sxs-lookup"><span data-stu-id="4565d-106">The result is a number in the current unit of measure for angles.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4565d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4565d-107">Syntax</span></span>

<span data-ttu-id="4565d-108">ATAN2(\*\* *y* \*\*, \*\* *x* \*\* )</span><span class="sxs-lookup"><span data-stu-id="4565d-108">ATAN2(\*\* *y* \*\*, \*\* *x* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4565d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4565d-109">Parameters</span></span>

|<span data-ttu-id="4565d-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="4565d-110">**Name**</span></span>|<span data-ttu-id="4565d-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="4565d-111">**Required/Optional**</span></span>|<span data-ttu-id="4565d-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4565d-112">**Data Type**</span></span>|<span data-ttu-id="4565d-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4565d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4565d-114">_y_</span><span class="sxs-lookup"><span data-stu-id="4565d-114">_y_</span></span> <br/> |<span data-ttu-id="4565d-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4565d-115">Required</span></span>  <br/> |<span data-ttu-id="4565d-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="4565d-116">**Numeric**</span></span> <br/> |<span data-ttu-id="4565d-117">Valor  _y_ del punto.</span><span class="sxs-lookup"><span data-stu-id="4565d-117">The  _y_-value of the point.</span></span>  <br/> |
| <span data-ttu-id="4565d-118">_x_</span><span class="sxs-lookup"><span data-stu-id="4565d-118">_x_</span></span> <br/> |<span data-ttu-id="4565d-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4565d-119">Required</span></span>  <br/> |<span data-ttu-id="4565d-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="4565d-120">**Numeric**</span></span> <br/> |<span data-ttu-id="4565d-121">El  _valor x_ del punto.</span><span class="sxs-lookup"><span data-stu-id="4565d-121">The  _x_-value of the point.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4565d-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4565d-122">Remarks</span></span>

<span data-ttu-id="4565d-123">La arco tangente es el ángulo medido en sentido contrario a las agujas del reloj desde el eje  *x*  positivo a una línea que interseca el origen (0,0) y el punto representado por  *x*  e  *y*  .</span><span class="sxs-lookup"><span data-stu-id="4565d-123">The arctangent is the angle measured counterclockwise from the positive  *x*  -axis to a line that intersects the origin (0,0) and the point represented by  *x*  and  *y*  .</span></span> <span data-ttu-id="4565d-124">En Microsoft Office Visio, ATAN2(0;0) devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="4565d-124">In Microsoft Visio, ATAN2(0,0) returns 0.</span></span> <span data-ttu-id="4565d-125">Para hacer que los resultados de ATAN2 se den en una unidad de medida angular distinta, utilice la función DEG o RAD.</span><span class="sxs-lookup"><span data-stu-id="4565d-125">To force the result of ATAN2 into a different angular measurement, use the DEG or RAD function.</span></span> 
  
<span data-ttu-id="4565d-126">La función ATAN2 es la inversa de la función TAN.</span><span class="sxs-lookup"><span data-stu-id="4565d-126">The ATAN2 function is the antifunction of the TAN function.</span></span> <span data-ttu-id="4565d-127">La función ATAN2 devuelve el ángulo cuyo ángulo es igual a  *y*  dividido por  *x*  .</span><span class="sxs-lookup"><span data-stu-id="4565d-127">The ATAN2 function returns the angle whose angle is equal to  *y*  divided by  *x*  .</span></span> <span data-ttu-id="4565d-128">Si ATAN2(*y,x*) representa un ángulo en un triángulo rectángulo,  *y*  es el "lado opuesto" y  *x*  es el "lado adyacente", por lo que la función podría escribirse como ATAN2 (opuesto, adyacente).</span><span class="sxs-lookup"><span data-stu-id="4565d-128">If ATAN2(*y,x*) represents an angle in a right triangle,  *y*  is the "opposite side" and  *x*  is the "adjacent side," so the function could be written as ATAN2(opposite,adjacent).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4565d-129">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="4565d-129">Example 1</span></span>

<span data-ttu-id="4565d-130">ATAN2(1.25,2.25)</span><span class="sxs-lookup"><span data-stu-id="4565d-130">ATAN2(1.25,2.25)</span></span>
  
<span data-ttu-id="4565d-131">Devuelve 29,0456 grados.</span><span class="sxs-lookup"><span data-stu-id="4565d-131">Returns 29.0456 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4565d-132">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="4565d-132">Example 2</span></span>

<span data-ttu-id="4565d-133">ATAN2(1,SQRT(3))</span><span class="sxs-lookup"><span data-stu-id="4565d-133">ATAN2(1,SQRT(3))</span></span>
  
<span data-ttu-id="4565d-134">Devuelve 30 grados.</span><span class="sxs-lookup"><span data-stu-id="4565d-134">Returns 30 deg</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4565d-135">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="4565d-135">Example 3</span></span>

<span data-ttu-id="4565d-136">ATAN2(1,1)</span><span class="sxs-lookup"><span data-stu-id="4565d-136">ATAN2(1,1)</span></span>
  
<span data-ttu-id="4565d-137">Devuelve 45 grados.</span><span class="sxs-lookup"><span data-stu-id="4565d-137">Returns 45 deg</span></span>
  

