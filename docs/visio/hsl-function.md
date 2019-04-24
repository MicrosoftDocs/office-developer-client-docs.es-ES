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
description: Devuelve un valor que representa un índice en la paleta de colores del documento. Especifica un color por sus componentes de matiz, saturación y luminosidad.
ms.openlocfilehash: 55703239395c54beedf4b7383435253f9c37006f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329928"
---
# <a name="hsl-function"></a><span data-ttu-id="fb650-104">Función HSL</span><span class="sxs-lookup"><span data-stu-id="fb650-104">HSL Function</span></span>

<span data-ttu-id="fb650-105">Devuelve un valor que representa un índice en la paleta de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="fb650-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="fb650-106">Especifica un color por sus componentes de matiz, saturación y luminosidad.</span><span class="sxs-lookup"><span data-stu-id="fb650-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fb650-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb650-107">Syntax</span></span>

<span data-ttu-id="fb650-108">HSL (\* \* *matiz* \* \*, \* \* *saturación* \* \*, \* \* *luminosidad* \* \*)</span><span class="sxs-lookup"><span data-stu-id="fb650-108">HSL(\*\* *hue* \*\*, \*\* *saturation* \*\*, \*\* *luminosity* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fb650-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb650-109">Parameters</span></span>

|<span data-ttu-id="fb650-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="fb650-110">**Name**</span></span>|<span data-ttu-id="fb650-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="fb650-111">**Required/Optional**</span></span>|<span data-ttu-id="fb650-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="fb650-112">**Data Type**</span></span>|<span data-ttu-id="fb650-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb650-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fb650-114">_matiz_</span><span class="sxs-lookup"><span data-stu-id="fb650-114">_hue_</span></span> <br/> |<span data-ttu-id="fb650-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fb650-115">Required</span></span>  <br/> |<span data-ttu-id="fb650-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="fb650-116">**Number**</span></span> <br/> |<span data-ttu-id="fb650-117">El matiz del color, expresado como un número comprendido entre 0 y 239, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="fb650-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="fb650-118">_saturación_</span><span class="sxs-lookup"><span data-stu-id="fb650-118">_saturation_</span></span> <br/> |<span data-ttu-id="fb650-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fb650-119">Required</span></span>  <br/> |<span data-ttu-id="fb650-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="fb650-120">**Number**</span></span> <br/> |<span data-ttu-id="fb650-121">La saturación del color, expresada como un número comprendido entre 0 y 240, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="fb650-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="fb650-122">_luminosidad_</span><span class="sxs-lookup"><span data-stu-id="fb650-122">_luminosity_</span></span> <br/> |<span data-ttu-id="fb650-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fb650-123">Required</span></span>  <br/> |<span data-ttu-id="fb650-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="fb650-124">**Number**</span></span> <br/> | <span data-ttu-id="fb650-125">La luminosidad del color, expresada como un número comprendido entre 0 y 240, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="fb650-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fb650-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb650-126">Return value</span></span>

<span data-ttu-id="fb650-127">Número</span><span class="sxs-lookup"><span data-stu-id="fb650-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb650-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb650-128">Remarks</span></span>

<span data-ttu-id="fb650-129">Si el color que devuelve la función no forma parte de la paleta de colores del documento actual, se agregará a la lista de colores disponibles del documento.</span><span class="sxs-lookup"><span data-stu-id="fb650-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="fb650-130">La tabla siguiente muestra varios colores estándar y los valores correspondientes al matiz, saturación y luminosidad.</span><span class="sxs-lookup"><span data-stu-id="fb650-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="fb650-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="fb650-131">**Color**</span></span>|<span data-ttu-id="fb650-132">**Valor de matiz**</span><span class="sxs-lookup"><span data-stu-id="fb650-132">**Hue value**</span></span>|<span data-ttu-id="fb650-133">**Valor de saturación**</span><span class="sxs-lookup"><span data-stu-id="fb650-133">**Saturation value**</span></span>|<span data-ttu-id="fb650-134">**Valor de luminosidad**</span><span class="sxs-lookup"><span data-stu-id="fb650-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fb650-135">Negro</span><span class="sxs-lookup"><span data-stu-id="fb650-135">Black</span></span>  <br/> |<span data-ttu-id="fb650-136">comprendi</span><span class="sxs-lookup"><span data-stu-id="fb650-136">0</span></span>  <br/> |<span data-ttu-id="fb650-137">comprendi</span><span class="sxs-lookup"><span data-stu-id="fb650-137">0</span></span>  <br/> |<span data-ttu-id="fb650-138">apartado</span><span class="sxs-lookup"><span data-stu-id="fb650-138">24</span></span>  <br/> |
|<span data-ttu-id="fb650-139">Azul</span><span class="sxs-lookup"><span data-stu-id="fb650-139">Blue</span></span>  <br/> |<span data-ttu-id="fb650-140">160</span><span class="sxs-lookup"><span data-stu-id="fb650-140">160</span></span>  <br/> |<span data-ttu-id="fb650-141">240</span><span class="sxs-lookup"><span data-stu-id="fb650-141">240</span></span>  <br/> |<span data-ttu-id="fb650-142">120</span><span class="sxs-lookup"><span data-stu-id="fb650-142">120</span></span>  <br/> |
|<span data-ttu-id="fb650-143">Verde</span><span class="sxs-lookup"><span data-stu-id="fb650-143">Green</span></span>  <br/> |<span data-ttu-id="fb650-144">80</span><span class="sxs-lookup"><span data-stu-id="fb650-144">80</span></span>  <br/> |<span data-ttu-id="fb650-145">240</span><span class="sxs-lookup"><span data-stu-id="fb650-145">240</span></span>  <br/> |<span data-ttu-id="fb650-146">120</span><span class="sxs-lookup"><span data-stu-id="fb650-146">120</span></span>  <br/> |
|<span data-ttu-id="fb650-147">Aguamarina</span><span class="sxs-lookup"><span data-stu-id="fb650-147">Cyan</span></span>  <br/> |<span data-ttu-id="fb650-148">120</span><span class="sxs-lookup"><span data-stu-id="fb650-148">120</span></span>  <br/> |<span data-ttu-id="fb650-149">240</span><span class="sxs-lookup"><span data-stu-id="fb650-149">240</span></span>  <br/> |<span data-ttu-id="fb650-150">120</span><span class="sxs-lookup"><span data-stu-id="fb650-150">120</span></span>  <br/> |
|<span data-ttu-id="fb650-151">Rojo</span><span class="sxs-lookup"><span data-stu-id="fb650-151">Red</span></span>  <br/> |<span data-ttu-id="fb650-152">comprendi</span><span class="sxs-lookup"><span data-stu-id="fb650-152">0</span></span>  <br/> |<span data-ttu-id="fb650-153">240</span><span class="sxs-lookup"><span data-stu-id="fb650-153">240</span></span>  <br/> |<span data-ttu-id="fb650-154">120</span><span class="sxs-lookup"><span data-stu-id="fb650-154">120</span></span>  <br/> |
|<span data-ttu-id="fb650-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="fb650-155">Magenta</span></span>  <br/> |<span data-ttu-id="fb650-156">200</span><span class="sxs-lookup"><span data-stu-id="fb650-156">200</span></span>  <br/> |<span data-ttu-id="fb650-157">240</span><span class="sxs-lookup"><span data-stu-id="fb650-157">240</span></span>  <br/> |<span data-ttu-id="fb650-158">120</span><span class="sxs-lookup"><span data-stu-id="fb650-158">120</span></span>  <br/> |
|<span data-ttu-id="fb650-159">Amarillo</span><span class="sxs-lookup"><span data-stu-id="fb650-159">Yellow</span></span>  <br/> |<span data-ttu-id="fb650-160">40</span><span class="sxs-lookup"><span data-stu-id="fb650-160">40</span></span>  <br/> |<span data-ttu-id="fb650-161">240</span><span class="sxs-lookup"><span data-stu-id="fb650-161">240</span></span>  <br/> |<span data-ttu-id="fb650-162">120</span><span class="sxs-lookup"><span data-stu-id="fb650-162">120</span></span>  <br/> |
|<span data-ttu-id="fb650-163">Blanco</span><span class="sxs-lookup"><span data-stu-id="fb650-163">White</span></span>  <br/> |<span data-ttu-id="fb650-164">comprendi</span><span class="sxs-lookup"><span data-stu-id="fb650-164">0</span></span>  <br/> |<span data-ttu-id="fb650-165">comprendi</span><span class="sxs-lookup"><span data-stu-id="fb650-165">0</span></span>  <br/> |<span data-ttu-id="fb650-166">240</span><span class="sxs-lookup"><span data-stu-id="fb650-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="fb650-167">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb650-167">Example 1</span></span>

<span data-ttu-id="fb650-168">HSL (160240120)</span><span class="sxs-lookup"><span data-stu-id="fb650-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="fb650-169">Devuelve el índice del color azul.</span><span class="sxs-lookup"><span data-stu-id="fb650-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fb650-170">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="fb650-170">Example 2</span></span>

<span data-ttu-id="fb650-171">HSL (matiz (FillForegnd), SAT (FillForegnd), MIN (LUM (FillForegnd) + 100240))</span><span class="sxs-lookup"><span data-stu-id="fb650-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="fb650-172">Devuelve el índice de un color que refleja el de relleno en primer plano, aunque con mayor luminosidad.</span><span class="sxs-lookup"><span data-stu-id="fb650-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

