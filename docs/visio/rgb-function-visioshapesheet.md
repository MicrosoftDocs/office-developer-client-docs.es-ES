---
title: RGB Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Devuelve un valor que representa un índice en la paleta de colores del documento. Especifica un color mediante sus componentes rojos, verdes y azules, donde cada uno es un número en el rango de 0 a 255, ambos incluidos, o una expresión que da como resultado un número.
ms.openlocfilehash: 7fa129d3ed28441f619660ed0db035cde85979bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822987"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="4d3f8-104">RGB Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="4d3f8-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="4d3f8-105">Devuelve un valor que representa un índice en la paleta de colores del documento.</span><span class="sxs-lookup"><span data-stu-id="4d3f8-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="4d3f8-106">Especifica un color mediante sus componentes rojos, verdes y azules, donde cada uno es un número en el rango de 0 a 255, ambos incluidos, o una expresión que da como resultado un número.</span><span class="sxs-lookup"><span data-stu-id="4d3f8-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4d3f8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d3f8-107">Syntax</span></span>

<span data-ttu-id="4d3f8-108">RGB (** *rojo* **, ** *verde* **, ** *azul* **)</span><span class="sxs-lookup"><span data-stu-id="4d3f8-108">RGB(** *red* **, ** *green* **, ** *blue* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4d3f8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d3f8-109">Parameters</span></span>

|<span data-ttu-id="4d3f8-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="4d3f8-110">**Name**</span></span>|<span data-ttu-id="4d3f8-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="4d3f8-111">**Required/Optional**</span></span>|<span data-ttu-id="4d3f8-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4d3f8-112">**Data Type**</span></span>|<span data-ttu-id="4d3f8-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4d3f8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4d3f8-114">_rojo_</span><span class="sxs-lookup"><span data-stu-id="4d3f8-114">_red_</span></span> <br/> |<span data-ttu-id="4d3f8-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4d3f8-115">Required</span></span>  <br/> |<span data-ttu-id="4d3f8-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="4d3f8-116">**Number**</span></span> <br/> |<span data-ttu-id="4d3f8-117">El componente rojo.</span><span class="sxs-lookup"><span data-stu-id="4d3f8-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="4d3f8-118">_verde_</span><span class="sxs-lookup"><span data-stu-id="4d3f8-118">_green_</span></span> <br/> |<span data-ttu-id="4d3f8-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4d3f8-119">Required</span></span>  <br/> |<span data-ttu-id="4d3f8-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="4d3f8-120">**Number**</span></span> <br/> |<span data-ttu-id="4d3f8-121">El componente verde.</span><span class="sxs-lookup"><span data-stu-id="4d3f8-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="4d3f8-122">_azul_</span><span class="sxs-lookup"><span data-stu-id="4d3f8-122">_blue_</span></span> <br/> |<span data-ttu-id="4d3f8-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4d3f8-123">Required</span></span>  <br/> |<span data-ttu-id="4d3f8-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="4d3f8-124">**Nmber**</span></span> <br/> |<span data-ttu-id="4d3f8-125">El componente azul.</span><span class="sxs-lookup"><span data-stu-id="4d3f8-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4d3f8-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d3f8-126">Return value</span></span>

<span data-ttu-id="4d3f8-127">Number</span><span class="sxs-lookup"><span data-stu-id="4d3f8-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d3f8-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d3f8-128">Remarks</span></span>

<span data-ttu-id="4d3f8-129">Si el color que devuelve la función no forma parte de la paleta de colores del documento actual, se agrega.</span><span class="sxs-lookup"><span data-stu-id="4d3f8-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="4d3f8-130">La tabla siguiente muestra varios colores estándar y los valores de sus componentes rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="4d3f8-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="4d3f8-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="4d3f8-131">**Color**</span></span>|<span data-ttu-id="4d3f8-132">**Valor Red (rojo)**</span><span class="sxs-lookup"><span data-stu-id="4d3f8-132">**Red value**</span></span>|<span data-ttu-id="4d3f8-133">**Valor Green (verde)**</span><span class="sxs-lookup"><span data-stu-id="4d3f8-133">**Green value**</span></span>|<span data-ttu-id="4d3f8-134">**Valor azul**</span><span class="sxs-lookup"><span data-stu-id="4d3f8-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4d3f8-135">Negro</span><span class="sxs-lookup"><span data-stu-id="4d3f8-135">Black</span></span>  <br/> |<span data-ttu-id="4d3f8-136">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-136">0</span></span>  <br/> |<span data-ttu-id="4d3f8-137">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-137">0</span></span>  <br/> |<span data-ttu-id="4d3f8-138">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-138">0</span></span>  <br/> |
|<span data-ttu-id="4d3f8-139">Azul</span><span class="sxs-lookup"><span data-stu-id="4d3f8-139">Blue</span></span>  <br/> |<span data-ttu-id="4d3f8-140">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-140">0</span></span>  <br/> |<span data-ttu-id="4d3f8-141">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-141">0</span></span>  <br/> |<span data-ttu-id="4d3f8-142">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-142">255</span></span>  <br/> |
|<span data-ttu-id="4d3f8-143">Verde</span><span class="sxs-lookup"><span data-stu-id="4d3f8-143">Green</span></span>  <br/> |<span data-ttu-id="4d3f8-144">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-144">0</span></span>  <br/> |<span data-ttu-id="4d3f8-145">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-145">255</span></span>  <br/> |<span data-ttu-id="4d3f8-146">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-146">0</span></span>  <br/> |
|<span data-ttu-id="4d3f8-147">Cian</span><span class="sxs-lookup"><span data-stu-id="4d3f8-147">Cyan</span></span>  <br/> |<span data-ttu-id="4d3f8-148">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-148">0</span></span>  <br/> |<span data-ttu-id="4d3f8-149">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-149">255</span></span>  <br/> |<span data-ttu-id="4d3f8-150">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-150">255</span></span>  <br/> |
|<span data-ttu-id="4d3f8-151">Rojo</span><span class="sxs-lookup"><span data-stu-id="4d3f8-151">Red</span></span>  <br/> |<span data-ttu-id="4d3f8-152">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-152">255</span></span>  <br/> |<span data-ttu-id="4d3f8-153">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-153">0</span></span>  <br/> |<span data-ttu-id="4d3f8-154">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-154">0</span></span>  <br/> |
|<span data-ttu-id="4d3f8-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="4d3f8-155">Magenta</span></span>  <br/> |<span data-ttu-id="4d3f8-156">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-156">255</span></span>  <br/> |<span data-ttu-id="4d3f8-157">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-157">0</span></span>  <br/> |<span data-ttu-id="4d3f8-158">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-158">255</span></span>  <br/> |
|<span data-ttu-id="4d3f8-159">Amarillo</span><span class="sxs-lookup"><span data-stu-id="4d3f8-159">Yellow</span></span>  <br/> |<span data-ttu-id="4d3f8-160">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-160">255</span></span>  <br/> |<span data-ttu-id="4d3f8-161">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-161">255</span></span>  <br/> |<span data-ttu-id="4d3f8-162">0</span><span class="sxs-lookup"><span data-stu-id="4d3f8-162">0</span></span>  <br/> |
|<span data-ttu-id="4d3f8-163">Blanco</span><span class="sxs-lookup"><span data-stu-id="4d3f8-163">White</span></span>  <br/> |<span data-ttu-id="4d3f8-164">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-164">255</span></span>  <br/> |<span data-ttu-id="4d3f8-165">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-165">255</span></span>  <br/> |<span data-ttu-id="4d3f8-166">255</span><span class="sxs-lookup"><span data-stu-id="4d3f8-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="4d3f8-167">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d3f8-167">Example 1</span></span>

<span data-ttu-id="4d3f8-168">RGB(0,0,255)</span><span class="sxs-lookup"><span data-stu-id="4d3f8-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="4d3f8-169">Devuelve el índice del color azul.</span><span class="sxs-lookup"><span data-stu-id="4d3f8-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4d3f8-170">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="4d3f8-170">Example 2</span></span>

<span data-ttu-id="4d3f8-171">¡RGB (rojo (Sheet.1! FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="4d3f8-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="4d3f8-172">Devuelve el índice que corresponde a un color cuyo componente rojo coincide con el del relleno de primer plano en la Hoja.1.</span><span class="sxs-lookup"><span data-stu-id="4d3f8-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

