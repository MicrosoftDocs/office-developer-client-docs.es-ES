---
title: GRAVITY (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
localization_priority: Normal
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: Calcula el ángulo correcto de rotación de un bloque de texto para el giro de la forma indicada para evitar que el texto se desenlameja.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429288"
---
# <a name="gravity-function"></a><span data-ttu-id="edaf4-103">Función GRAVITY</span><span class="sxs-lookup"><span data-stu-id="edaf4-103">GRAVITY Function</span></span>

<span data-ttu-id="edaf4-104">Calcula el ángulo correcto de rotación de un bloque de texto para el giro de la forma indicada para evitar que el texto se desenlameja.</span><span class="sxs-lookup"><span data-stu-id="edaf4-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="edaf4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edaf4-105">Syntax</span></span>

<span data-ttu-id="edaf4-106">GRAVITY(\*\* *angle* \*\*,[ \*\* *limit1* \*\* ],[ \*\* *limit2* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="edaf4-106">GRAVITY(\*\* *angle* \*\*,[ \*\* *limit1* \*\* ],[ \*\* *limit2* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="edaf4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edaf4-107">Parameters</span></span>

|<span data-ttu-id="edaf4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="edaf4-108">**Name**</span></span>|<span data-ttu-id="edaf4-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="edaf4-109">**Required/Optional**</span></span>|<span data-ttu-id="edaf4-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="edaf4-110">**Data Type**</span></span>|<span data-ttu-id="edaf4-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="edaf4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="edaf4-112">_ángulo_</span><span class="sxs-lookup"><span data-stu-id="edaf4-112">_angle_</span></span> <br/> |<span data-ttu-id="edaf4-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="edaf4-113">Required</span></span>  <br/> |<span data-ttu-id="edaf4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="edaf4-114">**String**</span></span> <br/> | <span data-ttu-id="edaf4-115">Ángulo de la forma.</span><span class="sxs-lookup"><span data-stu-id="edaf4-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="edaf4-116">_limit1_</span><span class="sxs-lookup"><span data-stu-id="edaf4-116">_limit1_</span></span> <br/> |<span data-ttu-id="edaf4-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="edaf4-117">Optional</span></span>  <br/> |<span data-ttu-id="edaf4-118">**String**</span><span class="sxs-lookup"><span data-stu-id="edaf4-118">**String**</span></span> <br/> |<span data-ttu-id="edaf4-119">Primer límite de rotación.</span><span class="sxs-lookup"><span data-stu-id="edaf4-119">First limit of rotation.</span></span> <span data-ttu-id="edaf4-120">El límite predeterminado es de 90 grados.</span><span class="sxs-lookup"><span data-stu-id="edaf4-120">Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="edaf4-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="edaf4-121">_limit2_</span></span> <br/> |<span data-ttu-id="edaf4-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="edaf4-122">Optional</span></span>  <br/> |<span data-ttu-id="edaf4-123">**String**</span><span class="sxs-lookup"><span data-stu-id="edaf4-123">**String**</span></span> <br/> |<span data-ttu-id="edaf4-124">Segundo límite de rotación.</span><span class="sxs-lookup"><span data-stu-id="edaf4-124">Second limit of rotation.</span></span> <span data-ttu-id="edaf4-125">El límite predeterminado es de 270 grados.</span><span class="sxs-lookup"><span data-stu-id="edaf4-125">Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="edaf4-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edaf4-126">Return value</span></span>

<span data-ttu-id="edaf4-127">String</span><span class="sxs-lookup"><span data-stu-id="edaf4-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="edaf4-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edaf4-128">Remarks</span></span>

<span data-ttu-id="edaf4-129">La función GRAVITY se utiliza normalmente en la celda TxtAngle.</span><span class="sxs-lookup"><span data-stu-id="edaf4-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="edaf4-130">El valor devuelto es 180 grados si  _el ángulo_ está entre los valores especificados por  _limit1_ y  _limit2_; de lo contrario, el valor devuelto es 0 grados.</span><span class="sxs-lookup"><span data-stu-id="edaf4-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="edaf4-131">La función normaliza automáticamente todos los argumentos para que estén comprendidos entre 0 y 360 grados.</span><span class="sxs-lookup"><span data-stu-id="edaf4-131">All of the arguments are automatically normalized between 0 and 360 degrees by the function.</span></span> <span data-ttu-id="edaf4-132">Si en un argumento no se especifican las unidades, se supone que se trata de radianes.</span><span class="sxs-lookup"><span data-stu-id="edaf4-132">If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="edaf4-133">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="edaf4-133">Example 1</span></span>

<span data-ttu-id="edaf4-134">GRAVITY(Angle)</span><span class="sxs-lookup"><span data-stu-id="edaf4-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="edaf4-135">Devuelve 180 grados si  *el ángulo*  está entre 90 y 270 grados; de lo contrario, devuelve 0 grados.</span><span class="sxs-lookup"><span data-stu-id="edaf4-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="edaf4-136">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="edaf4-136">Example 2</span></span>

<span data-ttu-id="edaf4-137">GRAVITY(2)</span><span class="sxs-lookup"><span data-stu-id="edaf4-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="edaf4-138">Devuelve 180 grados, ya que 2 radianes es un valor angular comprendido entre 90 y 270 grados.</span><span class="sxs-lookup"><span data-stu-id="edaf4-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="edaf4-139">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="edaf4-139">Example 3</span></span>

<span data-ttu-id="edaf4-140">GRAVITY(100 grad, 110 grad, 290 grad)</span><span class="sxs-lookup"><span data-stu-id="edaf4-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="edaf4-141">Devuelve 0 grados.</span><span class="sxs-lookup"><span data-stu-id="edaf4-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="edaf4-142">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="edaf4-142">Example 4</span></span>

<span data-ttu-id="edaf4-143">GRAVITY(100 grad, 290 grad, 110 grad)</span><span class="sxs-lookup"><span data-stu-id="edaf4-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="edaf4-144">Devuelve 0 grados.</span><span class="sxs-lookup"><span data-stu-id="edaf4-144">Returns 0 degrees.</span></span>
  

