---
title: Función RGB (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Devuelve un valor que representa un índice en la paleta de colores del documento. Especifica un color por sus componentes rojo, verde y azul, donde cada uno de ellos es un número entre 0 y 255, ambos incluidos, o una expresión que da como resultado un número de ese tipo.
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426306"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="9936d-104">Función RGB (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="9936d-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="9936d-105">Devuelve un valor que representa un índice en la paleta de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="9936d-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="9936d-106">Especifica un color por sus componentes rojo, verde y azul, donde cada uno de ellos es un número entre 0 y 255, ambos incluidos, o una expresión que da como resultado un número de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="9936d-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9936d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9936d-107">Syntax</span></span>

<span data-ttu-id="9936d-108">RGB (\* \* *rojo* \* \*, \* \* *verde* \* \*, \* \* *azul* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9936d-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9936d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9936d-109">Parameters</span></span>

|<span data-ttu-id="9936d-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="9936d-110">**Name**</span></span>|<span data-ttu-id="9936d-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="9936d-111">**Required/Optional**</span></span>|<span data-ttu-id="9936d-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="9936d-112">**Data Type**</span></span>|<span data-ttu-id="9936d-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9936d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9936d-114">_roja_</span><span class="sxs-lookup"><span data-stu-id="9936d-114">_red_</span></span> <br/> |<span data-ttu-id="9936d-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9936d-115">Required</span></span>  <br/> |<span data-ttu-id="9936d-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="9936d-116">**Number**</span></span> <br/> |<span data-ttu-id="9936d-117">El componente rojo.</span><span class="sxs-lookup"><span data-stu-id="9936d-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="9936d-118">_Green_</span><span class="sxs-lookup"><span data-stu-id="9936d-118">_green_</span></span> <br/> |<span data-ttu-id="9936d-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9936d-119">Required</span></span>  <br/> |<span data-ttu-id="9936d-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="9936d-120">**Number**</span></span> <br/> |<span data-ttu-id="9936d-121">El componente verde.</span><span class="sxs-lookup"><span data-stu-id="9936d-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="9936d-122">_azul_</span><span class="sxs-lookup"><span data-stu-id="9936d-122">_blue_</span></span> <br/> |<span data-ttu-id="9936d-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9936d-123">Required</span></span>  <br/> |<span data-ttu-id="9936d-124">**Nmber**</span><span class="sxs-lookup"><span data-stu-id="9936d-124">**Nmber**</span></span> <br/> |<span data-ttu-id="9936d-125">El componente azul.</span><span class="sxs-lookup"><span data-stu-id="9936d-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9936d-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9936d-126">Return value</span></span>

<span data-ttu-id="9936d-127">Número</span><span class="sxs-lookup"><span data-stu-id="9936d-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9936d-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9936d-128">Remarks</span></span>

<span data-ttu-id="9936d-129">Si el color que devuelve la función no forma parte de la paleta de colores del documento actual, se agrega.</span><span class="sxs-lookup"><span data-stu-id="9936d-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="9936d-130">La tabla siguiente muestra varios colores estándar y los valores de sus componentes rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="9936d-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="9936d-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="9936d-131">**Color**</span></span>|<span data-ttu-id="9936d-132">**Valor rojo**</span><span class="sxs-lookup"><span data-stu-id="9936d-132">**Red value**</span></span>|<span data-ttu-id="9936d-133">**Valor verde**</span><span class="sxs-lookup"><span data-stu-id="9936d-133">**Green value**</span></span>|<span data-ttu-id="9936d-134">**Valor azul**</span><span class="sxs-lookup"><span data-stu-id="9936d-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9936d-135">Negro</span><span class="sxs-lookup"><span data-stu-id="9936d-135">Black</span></span>  <br/> |<span data-ttu-id="9936d-136">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-136">0</span></span>  <br/> |<span data-ttu-id="9936d-137">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-137">0</span></span>  <br/> |<span data-ttu-id="9936d-138">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-138">0</span></span>  <br/> |
|<span data-ttu-id="9936d-139">Azul</span><span class="sxs-lookup"><span data-stu-id="9936d-139">Blue</span></span>  <br/> |<span data-ttu-id="9936d-140">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-140">0</span></span>  <br/> |<span data-ttu-id="9936d-141">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-141">0</span></span>  <br/> |<span data-ttu-id="9936d-142">255</span><span class="sxs-lookup"><span data-stu-id="9936d-142">255</span></span>  <br/> |
|<span data-ttu-id="9936d-143">Verde</span><span class="sxs-lookup"><span data-stu-id="9936d-143">Green</span></span>  <br/> |<span data-ttu-id="9936d-144">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-144">0</span></span>  <br/> |<span data-ttu-id="9936d-145">255</span><span class="sxs-lookup"><span data-stu-id="9936d-145">255</span></span>  <br/> |<span data-ttu-id="9936d-146">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-146">0</span></span>  <br/> |
|<span data-ttu-id="9936d-147">Aguamarina</span><span class="sxs-lookup"><span data-stu-id="9936d-147">Cyan</span></span>  <br/> |<span data-ttu-id="9936d-148">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-148">0</span></span>  <br/> |<span data-ttu-id="9936d-149">255</span><span class="sxs-lookup"><span data-stu-id="9936d-149">255</span></span>  <br/> |<span data-ttu-id="9936d-150">255</span><span class="sxs-lookup"><span data-stu-id="9936d-150">255</span></span>  <br/> |
|<span data-ttu-id="9936d-151">Rojo</span><span class="sxs-lookup"><span data-stu-id="9936d-151">Red</span></span>  <br/> |<span data-ttu-id="9936d-152">255</span><span class="sxs-lookup"><span data-stu-id="9936d-152">255</span></span>  <br/> |<span data-ttu-id="9936d-153">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-153">0</span></span>  <br/> |<span data-ttu-id="9936d-154">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-154">0</span></span>  <br/> |
|<span data-ttu-id="9936d-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="9936d-155">Magenta</span></span>  <br/> |<span data-ttu-id="9936d-156">255</span><span class="sxs-lookup"><span data-stu-id="9936d-156">255</span></span>  <br/> |<span data-ttu-id="9936d-157">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-157">0</span></span>  <br/> |<span data-ttu-id="9936d-158">255</span><span class="sxs-lookup"><span data-stu-id="9936d-158">255</span></span>  <br/> |
|<span data-ttu-id="9936d-159">Amarillo</span><span class="sxs-lookup"><span data-stu-id="9936d-159">Yellow</span></span>  <br/> |<span data-ttu-id="9936d-160">255</span><span class="sxs-lookup"><span data-stu-id="9936d-160">255</span></span>  <br/> |<span data-ttu-id="9936d-161">255</span><span class="sxs-lookup"><span data-stu-id="9936d-161">255</span></span>  <br/> |<span data-ttu-id="9936d-162">comprendi</span><span class="sxs-lookup"><span data-stu-id="9936d-162">0</span></span>  <br/> |
|<span data-ttu-id="9936d-163">Blanco</span><span class="sxs-lookup"><span data-stu-id="9936d-163">White</span></span>  <br/> |<span data-ttu-id="9936d-164">255</span><span class="sxs-lookup"><span data-stu-id="9936d-164">255</span></span>  <br/> |<span data-ttu-id="9936d-165">255</span><span class="sxs-lookup"><span data-stu-id="9936d-165">255</span></span>  <br/> |<span data-ttu-id="9936d-166">255</span><span class="sxs-lookup"><span data-stu-id="9936d-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="9936d-167">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="9936d-167">Example 1</span></span>

<span data-ttu-id="9936d-168">RGB (0, 0255)</span><span class="sxs-lookup"><span data-stu-id="9936d-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="9936d-169">Devuelve el índice del color azul.</span><span class="sxs-lookup"><span data-stu-id="9936d-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9936d-170">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="9936d-170">Example 2</span></span>

<span data-ttu-id="9936d-171">RGB (rojo (hoja. 1! FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="9936d-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="9936d-172">Devuelve el índice que corresponde a un color cuyo componente rojo coincide con el del relleno de primer plano en la Hoja.1.</span><span class="sxs-lookup"><span data-stu-id="9936d-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

