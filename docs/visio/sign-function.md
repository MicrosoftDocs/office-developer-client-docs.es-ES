---
title: SIGN (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Devuelve un valor que representa el signo de un número.
ms.openlocfilehash: 5f812dc4313e15df5d66a919707e7cdbb79f94b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823255"
---
# <a name="sign-function"></a><span data-ttu-id="009bc-103">Función SIGN</span><span class="sxs-lookup"><span data-stu-id="009bc-103">SIGN Function</span></span>

<span data-ttu-id="009bc-104">Devuelve un valor que representa el signo de un número.</span><span class="sxs-lookup"><span data-stu-id="009bc-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="009bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="009bc-105">Syntax</span></span>

<span data-ttu-id="009bc-106">Inicio de sesión (** *número* **, ** *exploración de vulnerabilidades* **)</span><span class="sxs-lookup"><span data-stu-id="009bc-106">SIGN(** *number* **, ** *fuzz* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="009bc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="009bc-107">Parameters</span></span>

|<span data-ttu-id="009bc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="009bc-108">**Name**</span></span>|<span data-ttu-id="009bc-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="009bc-109">**Required/Optional**</span></span>|<span data-ttu-id="009bc-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="009bc-110">**Data Type**</span></span>|<span data-ttu-id="009bc-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="009bc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="009bc-112">_number_</span><span class="sxs-lookup"><span data-stu-id="009bc-112">_number_</span></span> <br/> |<span data-ttu-id="009bc-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="009bc-113">Required</span></span>  <br/> |<span data-ttu-id="009bc-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="009bc-114">**Numeric**</span></span> <br/> | <span data-ttu-id="009bc-115">El número del que desea determinar el signo.</span><span class="sxs-lookup"><span data-stu-id="009bc-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="009bc-116">_exploración de vulnerabilidades_</span><span class="sxs-lookup"><span data-stu-id="009bc-116">_fuzz_</span></span> <br/> |<span data-ttu-id="009bc-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="009bc-117">Optional</span></span>  <br/> |<span data-ttu-id="009bc-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="009bc-118">**Numeric**</span></span> <br/> |<span data-ttu-id="009bc-119">Especifica cuánto puede diferenciarse un número de cero para seguir considerándose igual a cero.</span><span class="sxs-lookup"><span data-stu-id="009bc-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="009bc-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="009bc-120">Return value</span></span>

<span data-ttu-id="009bc-121">Numeric</span><span class="sxs-lookup"><span data-stu-id="009bc-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="009bc-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="009bc-122">Remarks</span></span>

<span data-ttu-id="009bc-123">La función SIGN devuelve 1 si el _número_ es positivo, 0 si el _número_ es cero o -1 si el _número_ es negativo.</span><span class="sxs-lookup"><span data-stu-id="009bc-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="009bc-124">Specifyin un valor de _aproximación_ ayuda a evitar errores de redondeo de punto flotante cuando un cálculo sea casi cero.</span><span class="sxs-lookup"><span data-stu-id="009bc-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="009bc-125">Si no especifica un valor de _aproximación_ , Visio utiliza 1E-9 (0,000000001).</span><span class="sxs-lookup"><span data-stu-id="009bc-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="009bc-126">Es posible que desee proporcionar un valor diferente cuando se aplica una escala dibujos o cuando desee que una comparación exacta.</span><span class="sxs-lookup"><span data-stu-id="009bc-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="009bc-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="009bc-127">Example 1</span></span>

<span data-ttu-id="009bc-128">SIGN(-5)</span><span class="sxs-lookup"><span data-stu-id="009bc-128">SIGN(-5)</span></span>
  
<span data-ttu-id="009bc-129">Devuelve -1.</span><span class="sxs-lookup"><span data-stu-id="009bc-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="009bc-130">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="009bc-130">Example 2</span></span>

<span data-ttu-id="009bc-131">SIGN(0)</span><span class="sxs-lookup"><span data-stu-id="009bc-131">SIGN(0)</span></span>
  
<span data-ttu-id="009bc-132">Devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="009bc-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="009bc-133">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="009bc-133">Example 3</span></span>

<span data-ttu-id="009bc-134">SIGN(0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="009bc-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="009bc-135">Devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="009bc-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="009bc-136">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="009bc-136">Example 4</span></span>

<span data-ttu-id="009bc-137">SIGN(0.00000000001,0)</span><span class="sxs-lookup"><span data-stu-id="009bc-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="009bc-138">Devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="009bc-138">Returns 1.</span></span>
  
