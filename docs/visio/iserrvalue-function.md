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
description: 'Devuelve TRUE si el valor de referenciaDeCelda es el tipo de error #VALUE, donde un argumento de la fórmula es del tipo incorrecto. La función ISERRVALUE se usa en expresiones lógicas que hacen referencia a otra celda.'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317890"
---
# <a name="iserrvalue-function"></a><span data-ttu-id="6327b-104">Función ISERRVALUE</span><span class="sxs-lookup"><span data-stu-id="6327b-104">ISERRVALUE Function</span></span>

<span data-ttu-id="6327b-105">Devuelve TRUE si el valor de _referenciaDeCelda_ es el tipo de error #VALUE, donde un argumento de la fórmula es del tipo incorrecto.</span><span class="sxs-lookup"><span data-stu-id="6327b-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="6327b-106">La función ISERRVALUE se usa en expresiones lógicas que hacen referencia a otra celda.</span><span class="sxs-lookup"><span data-stu-id="6327b-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6327b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6327b-107">Syntax</span></span>

<span data-ttu-id="6327b-108">ISERRVALUE (\* \* *referenciaDeCelda* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6327b-108">ISERRVALUE(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6327b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6327b-109">Parameters</span></span>

|<span data-ttu-id="6327b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="6327b-110">**Name**</span></span>|<span data-ttu-id="6327b-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="6327b-111">**Required/Optional**</span></span>|<span data-ttu-id="6327b-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="6327b-112">**Data Type**</span></span>|<span data-ttu-id="6327b-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6327b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6327b-114">_referenciaDeCelda_</span><span class="sxs-lookup"><span data-stu-id="6327b-114">_cellreference_</span></span> <br/> |<span data-ttu-id="6327b-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6327b-115">Required</span></span>  <br/> |<span data-ttu-id="6327b-116">**String**</span><span class="sxs-lookup"><span data-stu-id="6327b-116">**String**</span></span> <br/> |<span data-ttu-id="6327b-117">Referencia a una celda.</span><span class="sxs-lookup"><span data-stu-id="6327b-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6327b-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6327b-118">Remarks</span></span>

<span data-ttu-id="6327b-p103">Las celdas A a D de borrador no devuelven nuca un error #VALUE! ya que sus fórmulas pueden contener números y letras dentro de la misma cadena. Las celdas de la X a la Y deben contener sólo números.</span><span class="sxs-lookup"><span data-stu-id="6327b-p103">Scratch cells A through D won't return a #VALUE! error because the formula can contain numbers and letters in the same string. Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6327b-122">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="6327b-122">Example 1</span></span>

|<span data-ttu-id="6327b-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="6327b-123">**Cell**</span></span>|<span data-ttu-id="6327b-124">**Formula**</span><span class="sxs-lookup"><span data-stu-id="6327b-124">**Formula**</span></span>|<span data-ttu-id="6327b-125">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="6327b-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6327b-126">Grietas. x1</span><span class="sxs-lookup"><span data-stu-id="6327b-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="6327b-127">="Casa"</span><span class="sxs-lookup"><span data-stu-id="6327b-127">= "House"</span></span>  <br/> |<span data-ttu-id="6327b-128">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="6327b-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="6327b-129">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="6327b-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="6327b-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="6327b-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="6327b-131">segundo</span><span class="sxs-lookup"><span data-stu-id="6327b-131">2</span></span>  <br/> |
   
<span data-ttu-id="6327b-p104">Devuelve 2 ya que el valor devuelto es un error del tipo #VALUE! y la expresión indica a Microsoft Visio que debe devolver un 2 en lugar del error.</span><span class="sxs-lookup"><span data-stu-id="6327b-p104">Returns 2 because the value returned is a #VALUE! error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6327b-134">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="6327b-134">Example 2</span></span>

|<span data-ttu-id="6327b-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="6327b-135">**Cell**</span></span>|<span data-ttu-id="6327b-136">**Formula**</span><span class="sxs-lookup"><span data-stu-id="6327b-136">**Formula**</span></span>|<span data-ttu-id="6327b-137">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="6327b-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6327b-138">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="6327b-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="6327b-139">="5 + 7"</span><span class="sxs-lookup"><span data-stu-id="6327b-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="6327b-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="6327b-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="6327b-141">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="6327b-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="6327b-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="6327b-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="6327b-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="6327b-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="6327b-p105">Devuelve 12 ya que el valor devuelto no es un error del tipo #VALUE! y la expresión indica a Visio que debe devolver el valor de la celda original.</span><span class="sxs-lookup"><span data-stu-id="6327b-p105">Returns 12 because the value returned is not a #VALUE! error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

