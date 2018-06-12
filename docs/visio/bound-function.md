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
ms.openlocfilehash: 2f6228828fee8fa1831bb0d3a714fca068808652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821703"
---
# <a name="bound-function"></a><span data-ttu-id="a0b60-103">BOUND (función)</span><span class="sxs-lookup"><span data-stu-id="a0b60-103">BOUND Function</span></span>

<span data-ttu-id="a0b60-104">Restringe el valor de una celda a un intervalo o conjunto de intervalos.</span><span class="sxs-lookup"><span data-stu-id="a0b60-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a0b60-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0b60-105">Syntax</span></span>

<span data-ttu-id="a0b60-106">ENLAZADO (** *valor* **, ** *tipo* **, ** *Omitir* **, ** *valor1* **, ** *valor2* ** ** * [, omitir, value1(n), valor2,...] * **)</span><span class="sxs-lookup"><span data-stu-id="a0b60-106">BOUND (** *value* **, ** *type* **, ** *ignore* **, ** *value1* **, ** *value2* ** ** * [,ignore(n), value1(n), value2(n),...] * ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a0b60-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0b60-107">Parameters</span></span>

|<span data-ttu-id="a0b60-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a0b60-108">**Name**</span></span>|<span data-ttu-id="a0b60-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="a0b60-109">**Required/Optional**</span></span>|<span data-ttu-id="a0b60-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a0b60-110">**Data Type**</span></span>|<span data-ttu-id="a0b60-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0b60-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a0b60-112">_value_</span><span class="sxs-lookup"><span data-stu-id="a0b60-112">_value_</span></span> <br/> |<span data-ttu-id="a0b60-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a0b60-113">Required</span></span>  <br/> |<span data-ttu-id="a0b60-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="a0b60-114">**Numeric**</span></span> <br/> |<span data-ttu-id="a0b60-115">Valor actual que se ha de restringir.</span><span class="sxs-lookup"><span data-stu-id="a0b60-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="a0b60-116">_type_</span><span class="sxs-lookup"><span data-stu-id="a0b60-116">_type_</span></span> <br/> |<span data-ttu-id="a0b60-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a0b60-117">Required</span></span>  <br/> |<span data-ttu-id="a0b60-118">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="a0b60-118">**Numeric**</span></span> <br/> |<span data-ttu-id="a0b60-119">Si la restricción es inclusiva (0), exclusiva (1) o deshabilitado (2).</span><span class="sxs-lookup"><span data-stu-id="a0b60-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="a0b60-120">_Omitir_</span><span class="sxs-lookup"><span data-stu-id="a0b60-120">_ignore_</span></span> <br/> |<span data-ttu-id="a0b60-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a0b60-121">Required</span></span>  <br/> |<span data-ttu-id="a0b60-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a0b60-122">**Boolean**</span></span> <br/> | <span data-ttu-id="a0b60-123">TRUE omite el intervalo; FALSE restringe el valor de la celda al intervalo.</span><span class="sxs-lookup"><span data-stu-id="a0b60-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="a0b60-124">_valor1_</span><span class="sxs-lookup"><span data-stu-id="a0b60-124">_value1_</span></span> <br/> |<span data-ttu-id="a0b60-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a0b60-125">Required</span></span>  <br/> |<span data-ttu-id="a0b60-126">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="a0b60-126">**Numeric**</span></span> <br/> |<span data-ttu-id="a0b60-127">Primer valor en un rango.</span><span class="sxs-lookup"><span data-stu-id="a0b60-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="a0b60-128">_valor2_</span><span class="sxs-lookup"><span data-stu-id="a0b60-128">_value2_</span></span> <br/> |<span data-ttu-id="a0b60-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a0b60-129">Required</span></span>  <br/> |<span data-ttu-id="a0b60-130">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="a0b60-130">**Numeric**</span></span> <br/> |<span data-ttu-id="a0b60-131">Segundo valor de un intervalo.</span><span class="sxs-lookup"><span data-stu-id="a0b60-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0b60-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0b60-132">Remarks</span></span>

<span data-ttu-id="a0b60-133">Utilice la función BOUND para restringir una celda valor superior y límite inferior, por ejemplo, para controlar objetos que no se extiende por encima o por debajo de un alto mínimo o máximo.</span><span class="sxs-lookup"><span data-stu-id="a0b60-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="a0b60-134">La restricción puede ser exclusivo con respecto al intervalo o intervalos o ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="a0b60-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="a0b60-135">Si el valor actual no debe restringirse, establezca el parámetro de _tipo_ en 2 (desactivado).</span><span class="sxs-lookup"><span data-stu-id="a0b60-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="a0b60-136">Puede definir varios intervalos proporcionando varias apariciones de los parámetros de _Omitir_, _valor1_y _valor2_ .</span><span class="sxs-lookup"><span data-stu-id="a0b60-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="a0b60-137">Use el parámetro _Omitir_ para desactivar las restricciones en un intervalo determinado.</span><span class="sxs-lookup"><span data-stu-id="a0b60-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="a0b60-138">La fórmula que contiene la función BOUND no se sobrescribe cuando cambia su valor; en su lugar, la fórmula se mantiene y el nuevo valor se coloca en el parámetro _value_ .</span><span class="sxs-lookup"><span data-stu-id="a0b60-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a0b60-139">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="a0b60-139">Example 1</span></span>

<span data-ttu-id="a0b60-140">En este ejemplo se usa la función BOUND para forzar a un controlador a mantenerse en el interior del cuadro delimitador de una forma.</span><span class="sxs-lookup"><span data-stu-id="a0b60-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="a0b60-141">Controls.X1 = BOUND (Width\*0,5; 0; FALSE; Width\*0; Width\*1)</span><span class="sxs-lookup"><span data-stu-id="a0b60-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="a0b60-142">Controls.Y1 = BOUND (Height\*0,5; 0; FALSE; Height\*0; Height\*1)</span><span class="sxs-lookup"><span data-stu-id="a0b60-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a0b60-143">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="a0b60-143">Example 2</span></span>

<span data-ttu-id="a0b60-144">En este ejemplo se usa la función BOUND para restringir el ancho de una forma a 2, 4 ó 6 pulgadas.</span><span class="sxs-lookup"><span data-stu-id="a0b60-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="a0b60-145">Width = BOUND(; 0; FALSE; 2 in; 2 in; FALSE; 4 in; 4 in; FALSE; 6 in; 6 in)</span><span class="sxs-lookup"><span data-stu-id="a0b60-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

