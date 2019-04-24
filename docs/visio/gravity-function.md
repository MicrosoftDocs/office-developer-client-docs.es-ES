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
description: Calcula el ángulo de giro correcto del bloque de texto para la rotación de la forma indicada para evitar que el texto se gire hacia abajo.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360189"
---
# <a name="gravity-function"></a><span data-ttu-id="ce143-103">Función GRAVITY</span><span class="sxs-lookup"><span data-stu-id="ce143-103">GRAVITY Function</span></span>

<span data-ttu-id="ce143-104">Calcula el ángulo de giro correcto del bloque de texto para la rotación de la forma indicada para evitar que el texto se gire hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="ce143-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ce143-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce143-105">Syntax</span></span>

<span data-ttu-id="ce143-106">Gravity (\* \* *Angle* \* *, [* \* *límite1* \* *], [* \* *limit2* \* \*])</span><span class="sxs-lookup"><span data-stu-id="ce143-106">GRAVITY(\*\* *angle* \*\*,[ \*\* *limit1* \*\* ],[ \*\* *limit2* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ce143-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce143-107">Parameters</span></span>

|<span data-ttu-id="ce143-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ce143-108">**Name**</span></span>|<span data-ttu-id="ce143-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="ce143-109">**Required/Optional**</span></span>|<span data-ttu-id="ce143-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ce143-110">**Data Type**</span></span>|<span data-ttu-id="ce143-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce143-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ce143-112">_respecto_</span><span class="sxs-lookup"><span data-stu-id="ce143-112">_angle_</span></span> <br/> |<span data-ttu-id="ce143-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ce143-113">Required</span></span>  <br/> |<span data-ttu-id="ce143-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ce143-114">**String**</span></span> <br/> | <span data-ttu-id="ce143-115">Ángulo de la forma.</span><span class="sxs-lookup"><span data-stu-id="ce143-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="ce143-116">_límite1_</span><span class="sxs-lookup"><span data-stu-id="ce143-116">_limit1_</span></span> <br/> |<span data-ttu-id="ce143-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="ce143-117">Optional</span></span>  <br/> |<span data-ttu-id="ce143-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ce143-118">**String**</span></span> <br/> |<span data-ttu-id="ce143-119">Primer límite de rotación.</span><span class="sxs-lookup"><span data-stu-id="ce143-119">First limit of rotation.</span></span> <span data-ttu-id="ce143-120">El límite predeterminado es de 90 grados.</span><span class="sxs-lookup"><span data-stu-id="ce143-120">Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="ce143-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="ce143-121">_limit2_</span></span> <br/> |<span data-ttu-id="ce143-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="ce143-122">Optional</span></span>  <br/> |<span data-ttu-id="ce143-123">**String**</span><span class="sxs-lookup"><span data-stu-id="ce143-123">**String**</span></span> <br/> |<span data-ttu-id="ce143-124">Segundo límite de rotación.</span><span class="sxs-lookup"><span data-stu-id="ce143-124">Second limit of rotation.</span></span> <span data-ttu-id="ce143-125">El límite predeterminado es de 270 grados.</span><span class="sxs-lookup"><span data-stu-id="ce143-125">Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ce143-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce143-126">Return value</span></span>

<span data-ttu-id="ce143-127">String</span><span class="sxs-lookup"><span data-stu-id="ce143-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ce143-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce143-128">Remarks</span></span>

<span data-ttu-id="ce143-129">La función GRAVITY se utiliza normalmente en la celda TxtAngle.</span><span class="sxs-lookup"><span data-stu-id="ce143-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="ce143-130">El valor devuelto es 180 grados si el _ángulo_ está comprendido entre los valores especificados por _límite1_ y _limit2_; de lo contrario, el valor devuelto es 0 grados.</span><span class="sxs-lookup"><span data-stu-id="ce143-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="ce143-131">La función normaliza automáticamente todos los argumentos para que estén comprendidos entre 0 y 360 grados.</span><span class="sxs-lookup"><span data-stu-id="ce143-131">All of the arguments are automatically normalized between 0 and 360 degrees by the function.</span></span> <span data-ttu-id="ce143-132">Si en un argumento no se especifican las unidades, se supone que se trata de radianes.</span><span class="sxs-lookup"><span data-stu-id="ce143-132">If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ce143-133">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce143-133">Example 1</span></span>

<span data-ttu-id="ce143-134">GRAVEDAD (ángulo)</span><span class="sxs-lookup"><span data-stu-id="ce143-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="ce143-135">Devuelve 180 grados si el *ángulo* está entre 90 y 270 grados; de lo contrario, devuelve 0 grados.</span><span class="sxs-lookup"><span data-stu-id="ce143-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="ce143-136">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce143-136">Example 2</span></span>

<span data-ttu-id="ce143-137">GRAVEDAD (2)</span><span class="sxs-lookup"><span data-stu-id="ce143-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="ce143-138">Devuelve 180 grados, ya que 2 radianes es un valor angular comprendido entre 90 y 270 grados.</span><span class="sxs-lookup"><span data-stu-id="ce143-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ce143-139">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="ce143-139">Example 3</span></span>

<span data-ttu-id="ce143-140">GRAVITY(100 grad, 110 grad, 290 grad)</span><span class="sxs-lookup"><span data-stu-id="ce143-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="ce143-141">Devuelve 0 grados.</span><span class="sxs-lookup"><span data-stu-id="ce143-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="ce143-142">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="ce143-142">Example 4</span></span>

<span data-ttu-id="ce143-143">GRAVITY(100 grad, 290 grad, 110 grad)</span><span class="sxs-lookup"><span data-stu-id="ce143-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="ce143-144">Devuelve 0 grados.</span><span class="sxs-lookup"><span data-stu-id="ce143-144">Returns 0 degrees.</span></span>
  

