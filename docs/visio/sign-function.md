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
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420657"
---
# <a name="sign-function"></a><span data-ttu-id="4e0bd-103">Función SIGN</span><span class="sxs-lookup"><span data-stu-id="4e0bd-103">SIGN Function</span></span>

<span data-ttu-id="4e0bd-104">Devuelve un valor que representa el signo de un número.</span><span class="sxs-lookup"><span data-stu-id="4e0bd-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4e0bd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e0bd-105">Syntax</span></span>

<span data-ttu-id="4e0bd-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span><span class="sxs-lookup"><span data-stu-id="4e0bd-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4e0bd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e0bd-107">Parameters</span></span>

|<span data-ttu-id="4e0bd-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4e0bd-108">**Name**</span></span>|<span data-ttu-id="4e0bd-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="4e0bd-109">**Required/Optional**</span></span>|<span data-ttu-id="4e0bd-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4e0bd-110">**Data Type**</span></span>|<span data-ttu-id="4e0bd-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e0bd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4e0bd-112">_number_</span><span class="sxs-lookup"><span data-stu-id="4e0bd-112">_number_</span></span> <br/> |<span data-ttu-id="4e0bd-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4e0bd-113">Required</span></span>  <br/> |<span data-ttu-id="4e0bd-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="4e0bd-114">**Numeric**</span></span> <br/> | <span data-ttu-id="4e0bd-115">El número del que desea determinar el signo.</span><span class="sxs-lookup"><span data-stu-id="4e0bd-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="4e0bd-116">_fuzz_</span><span class="sxs-lookup"><span data-stu-id="4e0bd-116">_fuzz_</span></span> <br/> |<span data-ttu-id="4e0bd-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="4e0bd-117">Optional</span></span>  <br/> |<span data-ttu-id="4e0bd-118">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="4e0bd-118">**Numeric**</span></span> <br/> |<span data-ttu-id="4e0bd-119">Especifica cuánto puede diferenciarse un número de cero para seguir considerándose igual a cero.</span><span class="sxs-lookup"><span data-stu-id="4e0bd-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4e0bd-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e0bd-120">Return value</span></span>

<span data-ttu-id="4e0bd-121">Numérico</span><span class="sxs-lookup"><span data-stu-id="4e0bd-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e0bd-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e0bd-122">Remarks</span></span>

<span data-ttu-id="4e0bd-123">La función SIGN devuelve 1 si  _el número_ es positivo, 0 si  _el_ número es cero o -1 si  _el número_ es negativo.</span><span class="sxs-lookup"><span data-stu-id="4e0bd-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="4e0bd-124">Specifyin a fuzz value  _helps_ avoid floating-point roundoff errors when a calculation is almost zero.</span><span class="sxs-lookup"><span data-stu-id="4e0bd-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="4e0bd-125">Si no especifica un valor _de_ difuso, Visio usa 1E-9 (0,000000001).</span><span class="sxs-lookup"><span data-stu-id="4e0bd-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="4e0bd-126">Puede interesarle usar un valor distinto en el caso de cambios de escala de dibujos o cuando desee realizar una comparación exacta.</span><span class="sxs-lookup"><span data-stu-id="4e0bd-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4e0bd-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e0bd-127">Example 1</span></span>

<span data-ttu-id="4e0bd-128">SIGN(-5)</span><span class="sxs-lookup"><span data-stu-id="4e0bd-128">SIGN(-5)</span></span>
  
<span data-ttu-id="4e0bd-129">Devuelve -1.</span><span class="sxs-lookup"><span data-stu-id="4e0bd-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4e0bd-130">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="4e0bd-130">Example 2</span></span>

<span data-ttu-id="4e0bd-131">SIGN(0)</span><span class="sxs-lookup"><span data-stu-id="4e0bd-131">SIGN(0)</span></span>
  
<span data-ttu-id="4e0bd-132">Devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="4e0bd-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4e0bd-133">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="4e0bd-133">Example 3</span></span>

<span data-ttu-id="4e0bd-134">SIGN(0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="4e0bd-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="4e0bd-135">Devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="4e0bd-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="4e0bd-136">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="4e0bd-136">Example 4</span></span>

<span data-ttu-id="4e0bd-137">SIGN(0.00000000001,0)</span><span class="sxs-lookup"><span data-stu-id="4e0bd-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="4e0bd-138">Devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="4e0bd-138">Returns 1.</span></span>
  

