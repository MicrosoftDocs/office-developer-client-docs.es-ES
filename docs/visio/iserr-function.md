---
title: ISERR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Devuelve TRUE si el valor de referenciaDeCelda es algún tipo de error excepto #N/A; de lo contrario, devuelve FALSE. La función ESERR se usa en fórmulas que hacen referencia a otra celda.'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297252"
---
# <a name="iserr-function"></a><span data-ttu-id="2e34f-104">Función ISERR</span><span class="sxs-lookup"><span data-stu-id="2e34f-104">ISERR Function</span></span>

<span data-ttu-id="2e34f-105">Devuelve TRUE si el valor de _referenciaDeCelda_ es algún tipo de error excepto #N/a; de lo contrario, devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="2e34f-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="2e34f-106">La función ESERR se usa en fórmulas que hacen referencia a otra celda.</span><span class="sxs-lookup"><span data-stu-id="2e34f-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2e34f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e34f-107">Syntax</span></span>

<span data-ttu-id="2e34f-108">ESERR (\* \* *referenciaDeCelda* \* \*)</span><span class="sxs-lookup"><span data-stu-id="2e34f-108">ISERR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2e34f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e34f-109">Parameters</span></span>

|<span data-ttu-id="2e34f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="2e34f-110">**Name**</span></span>|<span data-ttu-id="2e34f-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="2e34f-111">**Required/Optional**</span></span>|<span data-ttu-id="2e34f-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2e34f-112">**Data Type**</span></span>|<span data-ttu-id="2e34f-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e34f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2e34f-114">_referenciaDeCelda_</span><span class="sxs-lookup"><span data-stu-id="2e34f-114">_cellreference_</span></span> <br/> |<span data-ttu-id="2e34f-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2e34f-115">Required</span></span>  <br/> |<span data-ttu-id="2e34f-116">**String**</span><span class="sxs-lookup"><span data-stu-id="2e34f-116">**String**</span></span> <br/> |<span data-ttu-id="2e34f-117">Referencia a una celda.</span><span class="sxs-lookup"><span data-stu-id="2e34f-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="2e34f-118">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="2e34f-118">Example 1</span></span>

|<span data-ttu-id="2e34f-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="2e34f-119">**Cell**</span></span>|<span data-ttu-id="2e34f-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="2e34f-120">**Formula**</span></span>|<span data-ttu-id="2e34f-121">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="2e34f-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2e34f-122">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="2e34f-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="2e34f-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="2e34f-123">=NA( )</span></span>  <br/> |<span data-ttu-id="2e34f-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="2e34f-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="2e34f-125">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="2e34f-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="2e34f-126">= ESERR (Scratch. a1)</span><span class="sxs-lookup"><span data-stu-id="2e34f-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="2e34f-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="2e34f-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="2e34f-p103">Devuelve FALSE ya que #N/A! es un error que la función ISERR no reconoce. Utilice ISERROR para encontrar todos los tipos de errores.</span><span class="sxs-lookup"><span data-stu-id="2e34f-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2e34f-131">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="2e34f-131">Example 2</span></span>

|<span data-ttu-id="2e34f-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="2e34f-132">**Cell**</span></span>|<span data-ttu-id="2e34f-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="2e34f-133">**Formula**</span></span>|<span data-ttu-id="2e34f-134">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="2e34f-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2e34f-135">Grietas. x1</span><span class="sxs-lookup"><span data-stu-id="2e34f-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="2e34f-136">= "Casa"</span><span class="sxs-lookup"><span data-stu-id="2e34f-136">="House"</span></span>  <br/> |<span data-ttu-id="2e34f-137">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="2e34f-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="2e34f-138">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="2e34f-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="2e34f-139">= ESERR (Scratch. x1)</span><span class="sxs-lookup"><span data-stu-id="2e34f-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="2e34f-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="2e34f-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="2e34f-p104">Devuelve TRUE ya que #VALUE! es un error que la función ISERR reconoce.</span><span class="sxs-lookup"><span data-stu-id="2e34f-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

