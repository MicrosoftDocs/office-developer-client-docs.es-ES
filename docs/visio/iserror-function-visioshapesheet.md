---
title: Función ISERROR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Devuelve TRUE si el valor de cellreference es cualquier tipo de error; de lo contrario, devuelve FALSE. La función ISERROR se usa en fórmulas que hacen referencia a otra celda.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421546"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="3b9ce-104">Función ISERROR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="3b9ce-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="3b9ce-105">Devuelve TRUE si el valor de  _cellreference_ es cualquier tipo de error; de lo contrario, devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="3b9ce-106">La función ISERROR se usa en fórmulas que hacen referencia a otra celda.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3b9ce-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b9ce-107">Syntax</span></span>

<span data-ttu-id="3b9ce-108">ISERROR(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="3b9ce-108">ISERROR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3b9ce-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b9ce-109">Parameters</span></span>

|<span data-ttu-id="3b9ce-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="3b9ce-110">**Name**</span></span>|<span data-ttu-id="3b9ce-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="3b9ce-111">**Required/Optional**</span></span>|<span data-ttu-id="3b9ce-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="3b9ce-112">**Data Type**</span></span>|<span data-ttu-id="3b9ce-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b9ce-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3b9ce-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="3b9ce-114">_cellreference_</span></span> <br/> |<span data-ttu-id="3b9ce-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3b9ce-115">Required</span></span>  <br/> |<span data-ttu-id="3b9ce-116">**String**</span><span class="sxs-lookup"><span data-stu-id="3b9ce-116">**String**</span></span> <br/> |<span data-ttu-id="3b9ce-117">Referencia a una celda.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="3b9ce-118">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="3b9ce-118">Example 1</span></span>

|<span data-ttu-id="3b9ce-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3b9ce-119">**Cell**</span></span>|<span data-ttu-id="3b9ce-120">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="3b9ce-120">**Formula**</span></span>|<span data-ttu-id="3b9ce-121">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="3b9ce-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b9ce-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="3b9ce-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="3b9ce-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="3b9ce-123">=NA( )</span></span>  <br/> |<span data-ttu-id="3b9ce-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="3b9ce-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="3b9ce-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="3b9ce-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="3b9ce-126">=ISERROR(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="3b9ce-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="3b9ce-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="3b9ce-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="3b9ce-p103">Devuelve TRUE (verdadero) ya que #N/A! es un error que la función ISERROR reconoce. Se puede utilizar la función ISERR para encontrar todos los tipos de error con excepción del error #N/A!</span><span class="sxs-lookup"><span data-stu-id="3b9ce-p103">Returns TRUE because the #N/A! error is recognized by the ISERROR function. You can use ISERR to find all types but the #N/A! error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3b9ce-132">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="3b9ce-132">Example 2</span></span>

|<span data-ttu-id="3b9ce-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3b9ce-133">**Cell**</span></span>|<span data-ttu-id="3b9ce-134">**Fórmula**</span><span class="sxs-lookup"><span data-stu-id="3b9ce-134">**Formula**</span></span>|<span data-ttu-id="3b9ce-135">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="3b9ce-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b9ce-136">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="3b9ce-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="3b9ce-137">="House"</span><span class="sxs-lookup"><span data-stu-id="3b9ce-137">="House"</span></span>  <br/> |<span data-ttu-id="3b9ce-138">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="3b9ce-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="3b9ce-139">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="3b9ce-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="3b9ce-140">=ISERROR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="3b9ce-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="3b9ce-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="3b9ce-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="3b9ce-p104">Devuelve TRUE (verdadero) ya que #VALUE! es un error que la función ISERROR reconoce. Para construir una expresión en función del error #VALUE! se debe utilizar la función ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-p104">Returns TRUE because the #VALUE! error is recognized by the ISERROR function. To build an expression based on the #VALUE! error, use the ISERRVALUE function.</span></span>
  

