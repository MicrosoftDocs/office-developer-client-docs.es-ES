---
title: ISERRVALUE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Devuelve TRUE si el valor de referenciaDeCelda es error del tipo #VALUE, donde un argumento en la fórmula es del tipo correcto. La función ISERRVALUE se utiliza en expresiones lógicas que hacen referencia a otra celda.'
ms.openlocfilehash: 50c501cc404d9c5f80e0bd1261b3d3bcd7087de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822377"
---
# <a name="iserrvalue-function"></a><span data-ttu-id="5e7f0-104">Función ISERRVALUE</span><span class="sxs-lookup"><span data-stu-id="5e7f0-104">ISERRVALUE Function</span></span>

<span data-ttu-id="5e7f0-105">Devuelve TRUE si el valor de _referenciaDeCelda_ es error del tipo #VALUE, donde un argumento en la fórmula es del tipo correcto.</span><span class="sxs-lookup"><span data-stu-id="5e7f0-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="5e7f0-106">La función ISERRVALUE se utiliza en expresiones lógicas que hacen referencia a otra celda.</span><span class="sxs-lookup"><span data-stu-id="5e7f0-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5e7f0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e7f0-107">Syntax</span></span>

<span data-ttu-id="5e7f0-108">ISERRVALUE (** *referenciaDeCelda* **)</span><span class="sxs-lookup"><span data-stu-id="5e7f0-108">ISERRVALUE(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5e7f0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e7f0-109">Parameters</span></span>

|<span data-ttu-id="5e7f0-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5e7f0-110">**Name**</span></span>|<span data-ttu-id="5e7f0-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="5e7f0-111">**Required/Optional**</span></span>|<span data-ttu-id="5e7f0-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5e7f0-112">**Data Type**</span></span>|<span data-ttu-id="5e7f0-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e7f0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5e7f0-114">_referenciaDeCelda_</span><span class="sxs-lookup"><span data-stu-id="5e7f0-114">_cellreference_</span></span> <br/> |<span data-ttu-id="5e7f0-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5e7f0-115">Required</span></span>  <br/> |<span data-ttu-id="5e7f0-116">**String**</span><span class="sxs-lookup"><span data-stu-id="5e7f0-116">**String**</span></span> <br/> |<span data-ttu-id="5e7f0-117">Referencia a una celda.</span><span class="sxs-lookup"><span data-stu-id="5e7f0-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e7f0-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e7f0-118">Remarks</span></span>

<span data-ttu-id="5e7f0-p103">Las celdas A a D de borrador no devuelven nuca un error #VALUE! ya que sus fórmulas pueden contener números y letras dentro de la misma cadena. Las celdas de la X a la Y deben contener sólo números.</span><span class="sxs-lookup"><span data-stu-id="5e7f0-p103">Scratch cells A through D won't return a #VALUE! error because the formula can contain numbers and letters in the same string. Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="5e7f0-122">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="5e7f0-122">Example 1</span></span>

|<span data-ttu-id="5e7f0-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="5e7f0-123">**Cell**</span></span>|<span data-ttu-id="5e7f0-124">**Formula**</span><span class="sxs-lookup"><span data-stu-id="5e7f0-124">**Formula**</span></span>|<span data-ttu-id="5e7f0-125">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="5e7f0-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5e7f0-126">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="5e7f0-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="5e7f0-127">="Casa"</span><span class="sxs-lookup"><span data-stu-id="5e7f0-127">= "House"</span></span>  <br/> |<span data-ttu-id="5e7f0-128">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="5e7f0-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="5e7f0-129">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="5e7f0-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="5e7f0-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="5e7f0-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="5e7f0-131">2</span><span class="sxs-lookup"><span data-stu-id="5e7f0-131">2</span></span>  <br/> |
   
<span data-ttu-id="5e7f0-p104">Devuelve 2 ya que el valor devuelto es un error del tipo #VALUE! y la expresión indica a Microsoft Visio que debe devolver un 2 en lugar del error.</span><span class="sxs-lookup"><span data-stu-id="5e7f0-p104">Returns 2 because the value returned is a #VALUE! error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5e7f0-134">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="5e7f0-134">Example 2</span></span>

|<span data-ttu-id="5e7f0-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="5e7f0-135">**Cell**</span></span>|<span data-ttu-id="5e7f0-136">**Formula**</span><span class="sxs-lookup"><span data-stu-id="5e7f0-136">**Formula**</span></span>|<span data-ttu-id="5e7f0-137">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="5e7f0-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5e7f0-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="5e7f0-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="5e7f0-139">="5 + 7"</span><span class="sxs-lookup"><span data-stu-id="5e7f0-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="5e7f0-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="5e7f0-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="5e7f0-141">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="5e7f0-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="5e7f0-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="5e7f0-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="5e7f0-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="5e7f0-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="5e7f0-p105">Devuelve 12 ya que el valor devuelto no es un error del tipo #VALUE! y la expresión indica a Visio que debe devolver el valor de la celda original.</span><span class="sxs-lookup"><span data-stu-id="5e7f0-p105">Returns 12 because the value returned is not a #VALUE! error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

