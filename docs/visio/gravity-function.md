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
description: Calcula el ángulo correcto de un bloque de texto de rotación de la rotación de la forma indicada evitar que el texto quede hacia abajo.
ms.openlocfilehash: 0d8b0160c7e7d63fb5a272219a2694d35e6e6b61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822241"
---
# <a name="gravity-function"></a><span data-ttu-id="dddf9-103">Función GRAVITY</span><span class="sxs-lookup"><span data-stu-id="dddf9-103">GRAVITY Function</span></span>

<span data-ttu-id="dddf9-104">Calcula el ángulo correcto de un bloque de texto de rotación de la rotación de la forma indicada evitar que el texto quede hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="dddf9-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dddf9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dddf9-105">Syntax</span></span>

<span data-ttu-id="dddf9-106">GRAVITY (** *ángulo* **, [** *límite 1* **], [** *límite 2* **])</span><span class="sxs-lookup"><span data-stu-id="dddf9-106">GRAVITY(** *angle* **,[ ** *limit1* ** ],[ ** *limit2* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dddf9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dddf9-107">Parameters</span></span>

|<span data-ttu-id="dddf9-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="dddf9-108">**Name**</span></span>|<span data-ttu-id="dddf9-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="dddf9-109">**Required/Optional**</span></span>|<span data-ttu-id="dddf9-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="dddf9-110">**Data Type**</span></span>|<span data-ttu-id="dddf9-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dddf9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dddf9-112">_ángulo_</span><span class="sxs-lookup"><span data-stu-id="dddf9-112">_angle_</span></span> <br/> |<span data-ttu-id="dddf9-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="dddf9-113">Required</span></span>  <br/> |<span data-ttu-id="dddf9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="dddf9-114">**String**</span></span> <br/> | <span data-ttu-id="dddf9-115">Ángulo de la forma.</span><span class="sxs-lookup"><span data-stu-id="dddf9-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="dddf9-116">_límite 1_</span><span class="sxs-lookup"><span data-stu-id="dddf9-116">_limit1_</span></span> <br/> |<span data-ttu-id="dddf9-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="dddf9-117">Optional</span></span>  <br/> |<span data-ttu-id="dddf9-118">**String**</span><span class="sxs-lookup"><span data-stu-id="dddf9-118">**String**</span></span> <br/> |<span data-ttu-id="dddf9-p101">Primer límite de rotación. El límite predeterminado es de 90 grados.</span><span class="sxs-lookup"><span data-stu-id="dddf9-p101">First limit of rotation. Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="dddf9-121">_límite 2_</span><span class="sxs-lookup"><span data-stu-id="dddf9-121">_limit2_</span></span> <br/> |<span data-ttu-id="dddf9-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="dddf9-122">Optional</span></span>  <br/> |<span data-ttu-id="dddf9-123">**String**</span><span class="sxs-lookup"><span data-stu-id="dddf9-123">**String**</span></span> <br/> |<span data-ttu-id="dddf9-p102">Segundo límite de rotación. El límite predeterminado es de 270 grados.</span><span class="sxs-lookup"><span data-stu-id="dddf9-p102">Second limit of rotation. Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dddf9-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dddf9-126">Return value</span></span>

<span data-ttu-id="dddf9-127">String</span><span class="sxs-lookup"><span data-stu-id="dddf9-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dddf9-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dddf9-128">Remarks</span></span>

<span data-ttu-id="dddf9-129">La función GRAVITY se utiliza normalmente en la celda TxtAngle.</span><span class="sxs-lookup"><span data-stu-id="dddf9-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="dddf9-130">El valor devuelto es 180 grados si _ángulo_ está comprendido entre los valores especificados mediante _límite 1_ y _límite 2_; en caso contrario, el valor devuelto es 0 grados.</span><span class="sxs-lookup"><span data-stu-id="dddf9-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="dddf9-p103">La función normaliza automáticamente todos los argumentos para que estén comprendidos entre 0 y 360 grados. Si en un argumento no se especifican las unidades, se supone que se trata de radianes.</span><span class="sxs-lookup"><span data-stu-id="dddf9-p103">All of the arguments are automatically normalized between 0 and 360 degrees by the function. If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="dddf9-133">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="dddf9-133">Example 1</span></span>

<span data-ttu-id="dddf9-134">GRAVITY(ángulo)</span><span class="sxs-lookup"><span data-stu-id="dddf9-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="dddf9-135">Devuelve 180 grados si *ángulo* está comprendido entre 90 y 270 grados; de lo contrario, devuelve 0 grados.</span><span class="sxs-lookup"><span data-stu-id="dddf9-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="dddf9-136">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="dddf9-136">Example 2</span></span>

<span data-ttu-id="dddf9-137">GRAVITY(2)</span><span class="sxs-lookup"><span data-stu-id="dddf9-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="dddf9-138">Devuelve 180 grados, ya que 2 radianes es un valor angular comprendido entre 90 y 270 grados.</span><span class="sxs-lookup"><span data-stu-id="dddf9-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="dddf9-139">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="dddf9-139">Example 3</span></span>

<span data-ttu-id="dddf9-140">GRAVITY(100 grad, 110 grad, 290 grad)</span><span class="sxs-lookup"><span data-stu-id="dddf9-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="dddf9-141">Devuelve 0 grados.</span><span class="sxs-lookup"><span data-stu-id="dddf9-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="dddf9-142">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="dddf9-142">Example 4</span></span>

<span data-ttu-id="dddf9-143">GRAVITY(100 grad, 290 grad, 110 grad)</span><span class="sxs-lookup"><span data-stu-id="dddf9-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="dddf9-144">Devuelve 0 grados.</span><span class="sxs-lookup"><span data-stu-id="dddf9-144">Returns 0 degrees.</span></span>
  

