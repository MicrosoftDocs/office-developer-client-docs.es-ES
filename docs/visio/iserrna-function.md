---
title: ISERRNA (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Devuelve TRUE si el valor de referenciaDeCelda es el tipo de error #N/A! (no disponible); de lo contrario, devuelve FALSE. La función ISERRNA se usa en fórmulas que hacen referencia a otra celda.'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357263"
---
# <a name="iserrna-function"></a><span data-ttu-id="d16a4-105">Función ISERRNA</span><span class="sxs-lookup"><span data-stu-id="d16a4-105">ISERRNA Function</span></span>

<span data-ttu-id="d16a4-106">Devuelve TRUE si el valor de _referenciaDeCelda_ es el tipo de error #N/a!</span><span class="sxs-lookup"><span data-stu-id="d16a4-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="d16a4-107">(no disponible); de lo contrario, devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="d16a4-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="d16a4-108">La función ISERRNA se usa en fórmulas que hacen referencia a otra celda.</span><span class="sxs-lookup"><span data-stu-id="d16a4-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d16a4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d16a4-109">Syntax</span></span>

<span data-ttu-id="d16a4-110">ISERRNA (\* \* *referenciaDeCelda* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d16a4-110">ISERRNA(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d16a4-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d16a4-111">Parameters</span></span>

|<span data-ttu-id="d16a4-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="d16a4-112">**Name**</span></span>|<span data-ttu-id="d16a4-113">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="d16a4-113">**Required/Optional**</span></span>|<span data-ttu-id="d16a4-114">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="d16a4-114">**Data Type**</span></span>|<span data-ttu-id="d16a4-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d16a4-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d16a4-116">_referenciaDeCelda_</span><span class="sxs-lookup"><span data-stu-id="d16a4-116">_cellreference_</span></span> <br/> |<span data-ttu-id="d16a4-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d16a4-117">Required</span></span>  <br/> |<span data-ttu-id="d16a4-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d16a4-118">**String**</span></span> <br/> |<span data-ttu-id="d16a4-119">Referencia a una celda.</span><span class="sxs-lookup"><span data-stu-id="d16a4-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="d16a4-120">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="d16a4-120">Example 1</span></span>

|<span data-ttu-id="d16a4-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d16a4-121">**Cell**</span></span>|<span data-ttu-id="d16a4-122">**Formula**</span><span class="sxs-lookup"><span data-stu-id="d16a4-122">**Formula**</span></span>|<span data-ttu-id="d16a4-123">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="d16a4-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d16a4-124">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="d16a4-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="d16a4-125">="5 +3"</span><span class="sxs-lookup"><span data-stu-id="d16a4-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="d16a4-126">8,5</span><span class="sxs-lookup"><span data-stu-id="d16a4-126">"8"</span></span>  <br/> |
|<span data-ttu-id="d16a4-127">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="d16a4-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="d16a4-128">= ISERRNA (Scratch. a1)</span><span class="sxs-lookup"><span data-stu-id="d16a4-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="d16a4-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="d16a4-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="d16a4-130">Devuelve FALSE (falso), ya que el valor devuelto está disponible.</span><span class="sxs-lookup"><span data-stu-id="d16a4-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d16a4-131">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="d16a4-131">Example 2</span></span>

|<span data-ttu-id="d16a4-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="d16a4-132">**Cell**</span></span>|<span data-ttu-id="d16a4-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="d16a4-133">**Formula**</span></span>|<span data-ttu-id="d16a4-134">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="d16a4-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d16a4-135">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="d16a4-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="d16a4-136">=NA( )</span><span class="sxs-lookup"><span data-stu-id="d16a4-136">=NA( )</span></span>  <br/> |<span data-ttu-id="d16a4-137">#N/A!</span><span class="sxs-lookup"><span data-stu-id="d16a4-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="d16a4-138">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="d16a4-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="d16a4-139">= ISERRNA (Scratch. a1)</span><span class="sxs-lookup"><span data-stu-id="d16a4-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="d16a4-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="d16a4-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="d16a4-141">Devuelve TRUE (verdadero) ya que el valor devuelto es un error del tipo #N/A!</span><span class="sxs-lookup"><span data-stu-id="d16a4-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

