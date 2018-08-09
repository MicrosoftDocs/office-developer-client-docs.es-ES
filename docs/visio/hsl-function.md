---
title: HSL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
localization_priority: Normal
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Devuelve un valor que representa un índice en la paleta de colores del documento. Especifica un color por su matiz, saturación y componentes de luminosidad.
ms.openlocfilehash: 50f343d990157d831ac4ac43057d0a2b7fca63f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822297"
---
# <a name="hsl-function"></a><span data-ttu-id="5aaa3-104">Función HSL</span><span class="sxs-lookup"><span data-stu-id="5aaa3-104">HSL Function</span></span>

<span data-ttu-id="5aaa3-105">Devuelve un valor que representa un índice en la paleta de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="5aaa3-106">Especifica un color por su matiz, saturación y componentes de luminosidad.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5aaa3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aaa3-107">Syntax</span></span>

<span data-ttu-id="5aaa3-108">HSL (** *matiz* **, ** *saturación* **, ** *luminosidad* **)</span><span class="sxs-lookup"><span data-stu-id="5aaa3-108">HSL(** *hue* **, ** *saturation* **, ** *luminosity* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5aaa3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aaa3-109">Parameters</span></span>

|<span data-ttu-id="5aaa3-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-110">**Name**</span></span>|<span data-ttu-id="5aaa3-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-111">**Required/Optional**</span></span>|<span data-ttu-id="5aaa3-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-112">**Data Type**</span></span>|<span data-ttu-id="5aaa3-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5aaa3-114">_matiz_</span><span class="sxs-lookup"><span data-stu-id="5aaa3-114">_hue_</span></span> <br/> |<span data-ttu-id="5aaa3-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5aaa3-115">Required</span></span>  <br/> |<span data-ttu-id="5aaa3-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-116">**Number**</span></span> <br/> |<span data-ttu-id="5aaa3-117">El matiz del color, expresado como un número comprendido entre 0 y 239, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="5aaa3-118">_saturación_</span><span class="sxs-lookup"><span data-stu-id="5aaa3-118">_saturation_</span></span> <br/> |<span data-ttu-id="5aaa3-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5aaa3-119">Required</span></span>  <br/> |<span data-ttu-id="5aaa3-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-120">**Number**</span></span> <br/> |<span data-ttu-id="5aaa3-121">La saturación del color, expresada como un número comprendido entre 0 y 240, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="5aaa3-122">_luminosidad_</span><span class="sxs-lookup"><span data-stu-id="5aaa3-122">_luminosity_</span></span> <br/> |<span data-ttu-id="5aaa3-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5aaa3-123">Required</span></span>  <br/> |<span data-ttu-id="5aaa3-124">**Número**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-124">**Number**</span></span> <br/> | <span data-ttu-id="5aaa3-125">La luminosidad del color, expresada como un número comprendido entre 0 y 240, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5aaa3-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5aaa3-126">Return value</span></span>

<span data-ttu-id="5aaa3-127">Number</span><span class="sxs-lookup"><span data-stu-id="5aaa3-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5aaa3-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aaa3-128">Remarks</span></span>

<span data-ttu-id="5aaa3-129">Si el color que devuelve la función no forma parte de la paleta de colores del documento actual, se agregará a la lista de colores disponibles del documento.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="5aaa3-130">La tabla siguiente muestra varios colores estándar y los valores correspondientes al matiz, saturación y luminosidad.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="5aaa3-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-131">**Color**</span></span>|<span data-ttu-id="5aaa3-132">**Valor de matiz**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-132">**Hue value**</span></span>|<span data-ttu-id="5aaa3-133">**Valor de saturación**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-133">**Saturation value**</span></span>|<span data-ttu-id="5aaa3-134">**Valor de luminosidad**</span><span class="sxs-lookup"><span data-stu-id="5aaa3-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5aaa3-135">Negro</span><span class="sxs-lookup"><span data-stu-id="5aaa3-135">Black</span></span>  <br/> |<span data-ttu-id="5aaa3-136">0</span><span class="sxs-lookup"><span data-stu-id="5aaa3-136">0</span></span>  <br/> |<span data-ttu-id="5aaa3-137">0</span><span class="sxs-lookup"><span data-stu-id="5aaa3-137">0</span></span>  <br/> |<span data-ttu-id="5aaa3-138">24</span><span class="sxs-lookup"><span data-stu-id="5aaa3-138">24</span></span>  <br/> |
|<span data-ttu-id="5aaa3-139">Azul</span><span class="sxs-lookup"><span data-stu-id="5aaa3-139">Blue</span></span>  <br/> |<span data-ttu-id="5aaa3-140">160</span><span class="sxs-lookup"><span data-stu-id="5aaa3-140">160</span></span>  <br/> |<span data-ttu-id="5aaa3-141">240</span><span class="sxs-lookup"><span data-stu-id="5aaa3-141">240</span></span>  <br/> |<span data-ttu-id="5aaa3-142">120</span><span class="sxs-lookup"><span data-stu-id="5aaa3-142">120</span></span>  <br/> |
|<span data-ttu-id="5aaa3-143">Verde</span><span class="sxs-lookup"><span data-stu-id="5aaa3-143">Green</span></span>  <br/> |<span data-ttu-id="5aaa3-144">80</span><span class="sxs-lookup"><span data-stu-id="5aaa3-144">80</span></span>  <br/> |<span data-ttu-id="5aaa3-145">240</span><span class="sxs-lookup"><span data-stu-id="5aaa3-145">240</span></span>  <br/> |<span data-ttu-id="5aaa3-146">120</span><span class="sxs-lookup"><span data-stu-id="5aaa3-146">120</span></span>  <br/> |
|<span data-ttu-id="5aaa3-147">Cian</span><span class="sxs-lookup"><span data-stu-id="5aaa3-147">Cyan</span></span>  <br/> |<span data-ttu-id="5aaa3-148">120</span><span class="sxs-lookup"><span data-stu-id="5aaa3-148">120</span></span>  <br/> |<span data-ttu-id="5aaa3-149">240</span><span class="sxs-lookup"><span data-stu-id="5aaa3-149">240</span></span>  <br/> |<span data-ttu-id="5aaa3-150">120</span><span class="sxs-lookup"><span data-stu-id="5aaa3-150">120</span></span>  <br/> |
|<span data-ttu-id="5aaa3-151">Rojo</span><span class="sxs-lookup"><span data-stu-id="5aaa3-151">Red</span></span>  <br/> |<span data-ttu-id="5aaa3-152">0</span><span class="sxs-lookup"><span data-stu-id="5aaa3-152">0</span></span>  <br/> |<span data-ttu-id="5aaa3-153">240</span><span class="sxs-lookup"><span data-stu-id="5aaa3-153">240</span></span>  <br/> |<span data-ttu-id="5aaa3-154">120</span><span class="sxs-lookup"><span data-stu-id="5aaa3-154">120</span></span>  <br/> |
|<span data-ttu-id="5aaa3-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="5aaa3-155">Magenta</span></span>  <br/> |<span data-ttu-id="5aaa3-156">200</span><span class="sxs-lookup"><span data-stu-id="5aaa3-156">200</span></span>  <br/> |<span data-ttu-id="5aaa3-157">240</span><span class="sxs-lookup"><span data-stu-id="5aaa3-157">240</span></span>  <br/> |<span data-ttu-id="5aaa3-158">120</span><span class="sxs-lookup"><span data-stu-id="5aaa3-158">120</span></span>  <br/> |
|<span data-ttu-id="5aaa3-159">Amarillo</span><span class="sxs-lookup"><span data-stu-id="5aaa3-159">Yellow</span></span>  <br/> |<span data-ttu-id="5aaa3-160">40</span><span class="sxs-lookup"><span data-stu-id="5aaa3-160">40</span></span>  <br/> |<span data-ttu-id="5aaa3-161">240</span><span class="sxs-lookup"><span data-stu-id="5aaa3-161">240</span></span>  <br/> |<span data-ttu-id="5aaa3-162">120</span><span class="sxs-lookup"><span data-stu-id="5aaa3-162">120</span></span>  <br/> |
|<span data-ttu-id="5aaa3-163">Blanco</span><span class="sxs-lookup"><span data-stu-id="5aaa3-163">White</span></span>  <br/> |<span data-ttu-id="5aaa3-164">0</span><span class="sxs-lookup"><span data-stu-id="5aaa3-164">0</span></span>  <br/> |<span data-ttu-id="5aaa3-165">0</span><span class="sxs-lookup"><span data-stu-id="5aaa3-165">0</span></span>  <br/> |<span data-ttu-id="5aaa3-166">240</span><span class="sxs-lookup"><span data-stu-id="5aaa3-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="5aaa3-167">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="5aaa3-167">Example 1</span></span>

<span data-ttu-id="5aaa3-168">HSL(160;240;120)</span><span class="sxs-lookup"><span data-stu-id="5aaa3-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="5aaa3-169">Devuelve el índice del color azul.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5aaa3-170">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="5aaa3-170">Example 2</span></span>

<span data-ttu-id="5aaa3-171">HSL(Hue(FillForegnd),Sat(FillForegnd),min(Lum(FillForegnd)+100,240))</span><span class="sxs-lookup"><span data-stu-id="5aaa3-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="5aaa3-172">Devuelve el índice de un color que refleja el de relleno en primer plano, aunque con mayor luminosidad.</span><span class="sxs-lookup"><span data-stu-id="5aaa3-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

