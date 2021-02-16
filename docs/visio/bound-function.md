---
title: BOUND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Restringe el valor de una celda a un intervalo o conjunto de intervalos.
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425963"
---
# <a name="bound-function"></a><span data-ttu-id="bb8e4-103">Función BOUND</span><span class="sxs-lookup"><span data-stu-id="bb8e4-103">BOUND Function</span></span>

<span data-ttu-id="bb8e4-104">Restringe el valor de una celda a un intervalo o conjunto de intervalos.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bb8e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb8e4-105">Syntax</span></span>

<span data-ttu-id="bb8e4-106">BOUND (\*\* *value* \*\*, \*\* *type* \*\*, \*\* *ignore* \*\*, \*\* *value1* \*\*, \*\* *value2* \*\* \*\* \* [,ignore(n), value1(n), value2(n),...] \* \*\* )</span><span class="sxs-lookup"><span data-stu-id="bb8e4-106">BOUND (\*\* *value* \*\*, \*\* *type* \*\*, \*\* *ignore* \*\*, \*\* *value1* \*\*, \*\* *value2* \*\* \*\* \* [,ignore(n), value1(n), value2(n),...] \* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bb8e4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb8e4-107">Parameters</span></span>

|<span data-ttu-id="bb8e4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-108">**Name**</span></span>|<span data-ttu-id="bb8e4-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-109">**Required/Optional**</span></span>|<span data-ttu-id="bb8e4-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-110">**Data Type**</span></span>|<span data-ttu-id="bb8e4-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bb8e4-112">_value_</span><span class="sxs-lookup"><span data-stu-id="bb8e4-112">_value_</span></span> <br/> |<span data-ttu-id="bb8e4-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bb8e4-113">Required</span></span>  <br/> |<span data-ttu-id="bb8e4-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-114">**Numeric**</span></span> <br/> |<span data-ttu-id="bb8e4-115">Valor actual que se ha de restringir.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="bb8e4-116">_type_</span><span class="sxs-lookup"><span data-stu-id="bb8e4-116">_type_</span></span> <br/> |<span data-ttu-id="bb8e4-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bb8e4-117">Required</span></span>  <br/> |<span data-ttu-id="bb8e4-118">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-118">**Numeric**</span></span> <br/> |<span data-ttu-id="bb8e4-119">Indica si la restricción es inclusiva (0), exclusiva (1) o está deshabilitada (2).</span><span class="sxs-lookup"><span data-stu-id="bb8e4-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="bb8e4-120">_ignore_</span><span class="sxs-lookup"><span data-stu-id="bb8e4-120">_ignore_</span></span> <br/> |<span data-ttu-id="bb8e4-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bb8e4-121">Required</span></span>  <br/> |<span data-ttu-id="bb8e4-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-122">**Boolean**</span></span> <br/> | <span data-ttu-id="bb8e4-123">TRUE para omitir el rango; FALSE para restringir el valor de la celda al rango.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="bb8e4-124">_value1_</span><span class="sxs-lookup"><span data-stu-id="bb8e4-124">_value1_</span></span> <br/> |<span data-ttu-id="bb8e4-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bb8e4-125">Required</span></span>  <br/> |<span data-ttu-id="bb8e4-126">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-126">**Numeric**</span></span> <br/> |<span data-ttu-id="bb8e4-127">Primer valor de un intervalo.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="bb8e4-128">_value2_</span><span class="sxs-lookup"><span data-stu-id="bb8e4-128">_value2_</span></span> <br/> |<span data-ttu-id="bb8e4-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bb8e4-129">Required</span></span>  <br/> |<span data-ttu-id="bb8e4-130">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="bb8e4-130">**Numeric**</span></span> <br/> |<span data-ttu-id="bb8e4-131">Segundo valor de un intervalo.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb8e4-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb8e4-132">Remarks</span></span>

<span data-ttu-id="bb8e4-133">Use la función BOUND para restringir el valor de una celda entre un límite superior y uno inferior, por ejemplo, para controlar objetos que no deben estirarse más allá de una altura máxima o mínima.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="bb8e4-134">La restricción puede ser inclusiva o exclusiva con respecto a los intervalos.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="bb8e4-135">Si el valor actual no debe restringirse, establezca el parámetro  _de_ tipo en 2 (deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="bb8e4-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="bb8e4-136">Puede definir varios intervalos si proporciona varias repeticiones de los parámetros _ignore_, _value1_ y _value2._</span><span class="sxs-lookup"><span data-stu-id="bb8e4-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="bb8e4-137">Use el  _parámetro ignore_ para deshabilitar las restricciones de un intervalo determinado.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="bb8e4-138">La fórmula que contiene la función BOUND no se sobrescribe cuando cambia su valor; en su lugar, la fórmula se conserva y el nuevo valor se coloca en el  _parámetro de_ valor.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="bb8e4-139">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb8e4-139">Example 1</span></span>

<span data-ttu-id="bb8e4-140">En este ejemplo se usa la función BOUND para forzar a un controlador a mantenerse en el interior del cuadro delimitador de una forma.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="bb8e4-141">Controls.X1 = BOUND(Width \* 0.5, 0, FALSE, Width \* 0, Width \* 1)</span><span class="sxs-lookup"><span data-stu-id="bb8e4-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="bb8e4-142">Controls.Y1 = BOUND(Height \* 0.5, 0, FALSE, Height \* 0, Height \* 1)</span><span class="sxs-lookup"><span data-stu-id="bb8e4-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bb8e4-143">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="bb8e4-143">Example 2</span></span>

<span data-ttu-id="bb8e4-144">En este ejemplo se usa la función BOUND para restringir el ancho de una forma a 2, 4 ó 6 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="bb8e4-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="bb8e4-145">Width = BOUND(; 0; FALSE; 2 in; 2 in; FALSE; 4 in; 4 in; FALSE; 6 in; 6 in)</span><span class="sxs-lookup"><span data-stu-id="bb8e4-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

