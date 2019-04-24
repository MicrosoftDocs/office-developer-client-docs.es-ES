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
description: Devuelve TRUE si el valor de referenciaDeCelda es algún tipo de error; de lo contrario, devuelve FALSE. La función ISERROR se usa en fórmulas que hacen referencia a otra celda.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317895"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="b2788-104">Función ISERROR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="b2788-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="b2788-105">Devuelve TRUE si el valor de _referenciaDeCelda_ es algún tipo de error; de lo contrario, devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="b2788-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="b2788-106">La función ISERROR se usa en fórmulas que hacen referencia a otra celda.</span><span class="sxs-lookup"><span data-stu-id="b2788-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b2788-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2788-107">Syntax</span></span>

<span data-ttu-id="b2788-108">ISERROR (\* \* *referenciaDeCelda* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b2788-108">ISERROR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b2788-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2788-109">Parameters</span></span>

|<span data-ttu-id="b2788-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="b2788-110">**Name**</span></span>|<span data-ttu-id="b2788-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="b2788-111">**Required/Optional**</span></span>|<span data-ttu-id="b2788-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="b2788-112">**Data Type**</span></span>|<span data-ttu-id="b2788-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b2788-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b2788-114">_referenciaDeCelda_</span><span class="sxs-lookup"><span data-stu-id="b2788-114">_cellreference_</span></span> <br/> |<span data-ttu-id="b2788-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b2788-115">Required</span></span>  <br/> |<span data-ttu-id="b2788-116">**String**</span><span class="sxs-lookup"><span data-stu-id="b2788-116">**String**</span></span> <br/> |<span data-ttu-id="b2788-117">Referencia a una celda.</span><span class="sxs-lookup"><span data-stu-id="b2788-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="b2788-118">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2788-118">Example 1</span></span>

|<span data-ttu-id="b2788-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="b2788-119">**Cell**</span></span>|<span data-ttu-id="b2788-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="b2788-120">**Formula**</span></span>|<span data-ttu-id="b2788-121">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="b2788-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2788-122">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="b2788-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="b2788-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="b2788-123">=NA( )</span></span>  <br/> |<span data-ttu-id="b2788-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="b2788-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="b2788-125">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="b2788-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="b2788-126">= ISERROR (Scratch. a1)</span><span class="sxs-lookup"><span data-stu-id="b2788-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="b2788-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="b2788-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="b2788-p103">Devuelve TRUE (verdadero) ya que #N/A! es un error que la función ISERROR reconoce. Se puede utilizar la función ISERR para encontrar todos los tipos de error con excepción del error #N/A!</span><span class="sxs-lookup"><span data-stu-id="b2788-p103">Returns TRUE because the #N/A! error is recognized by the ISERROR function. You can use ISERR to find all types but the #N/A! error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b2788-132">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="b2788-132">Example 2</span></span>

|<span data-ttu-id="b2788-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="b2788-133">**Cell**</span></span>|<span data-ttu-id="b2788-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="b2788-134">**Formula**</span></span>|<span data-ttu-id="b2788-135">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="b2788-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2788-136">Grietas. x1</span><span class="sxs-lookup"><span data-stu-id="b2788-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="b2788-137">= "Casa"</span><span class="sxs-lookup"><span data-stu-id="b2788-137">="House"</span></span>  <br/> |<span data-ttu-id="b2788-138">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="b2788-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="b2788-139">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="b2788-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="b2788-140">= ISERROR (Scratch. x1)</span><span class="sxs-lookup"><span data-stu-id="b2788-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="b2788-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="b2788-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="b2788-p104">Devuelve TRUE (verdadero) ya que #VALUE! es un error que la función ISERROR reconoce. Para construir una expresión en función del error #VALUE! se debe utilizar la función ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="b2788-p104">Returns TRUE because the #VALUE! error is recognized by the ISERROR function. To build an expression based on the #VALUE! error, use the ISERRVALUE function.</span></span>
  

