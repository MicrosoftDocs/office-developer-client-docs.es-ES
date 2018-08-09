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
description: 'Devuelve TRUE si el valor de referenciaDeCelda es error del tipo #N/A! (no disponible); de lo contrario, devuelve FALSE. La función ISERRNA se utiliza en las fórmulas que hacen referencia a otra celda.'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822372"
---
# <a name="iserrna-function"></a><span data-ttu-id="bde34-105">Función ISERRNA</span><span class="sxs-lookup"><span data-stu-id="bde34-105">ISERRNA Function</span></span>

<span data-ttu-id="bde34-106">Devuelve TRUE si el valor de _referenciaDeCelda_ es error del tipo #N/A!</span><span class="sxs-lookup"><span data-stu-id="bde34-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="bde34-107">(no disponible); de lo contrario, devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="bde34-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="bde34-108">La función ISERRNA se utiliza en las fórmulas que hacen referencia a otra celda.</span><span class="sxs-lookup"><span data-stu-id="bde34-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bde34-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bde34-109">Syntax</span></span>

<span data-ttu-id="bde34-110">ISERRNA (** *referenciaDeCelda* **)</span><span class="sxs-lookup"><span data-stu-id="bde34-110">ISERRNA(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bde34-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bde34-111">Parameters</span></span>

|<span data-ttu-id="bde34-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="bde34-112">**Name**</span></span>|<span data-ttu-id="bde34-113">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="bde34-113">**Required/Optional**</span></span>|<span data-ttu-id="bde34-114">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="bde34-114">**Data Type**</span></span>|<span data-ttu-id="bde34-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bde34-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bde34-116">_referenciaDeCelda_</span><span class="sxs-lookup"><span data-stu-id="bde34-116">_cellreference_</span></span> <br/> |<span data-ttu-id="bde34-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bde34-117">Required</span></span>  <br/> |<span data-ttu-id="bde34-118">**String**</span><span class="sxs-lookup"><span data-stu-id="bde34-118">**String**</span></span> <br/> |<span data-ttu-id="bde34-119">Referencia a una celda.</span><span class="sxs-lookup"><span data-stu-id="bde34-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="bde34-120">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="bde34-120">Example 1</span></span>

|<span data-ttu-id="bde34-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="bde34-121">**Cell**</span></span>|<span data-ttu-id="bde34-122">**Formula**</span><span class="sxs-lookup"><span data-stu-id="bde34-122">**Formula**</span></span>|<span data-ttu-id="bde34-123">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="bde34-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bde34-124">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="bde34-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="bde34-125">="5 +3"</span><span class="sxs-lookup"><span data-stu-id="bde34-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="bde34-126">"8"</span><span class="sxs-lookup"><span data-stu-id="bde34-126">"8"</span></span>  <br/> |
|<span data-ttu-id="bde34-127">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="bde34-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="bde34-128">=ISERRNA(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="bde34-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="bde34-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="bde34-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="bde34-130">Devuelve FALSE (falso), ya que el valor devuelto está disponible.</span><span class="sxs-lookup"><span data-stu-id="bde34-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bde34-131">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="bde34-131">Example 2</span></span>

|<span data-ttu-id="bde34-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="bde34-132">**Cell**</span></span>|<span data-ttu-id="bde34-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="bde34-133">**Formula**</span></span>|<span data-ttu-id="bde34-134">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="bde34-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bde34-135">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="bde34-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="bde34-136">=NA( )</span><span class="sxs-lookup"><span data-stu-id="bde34-136">=NA( )</span></span>  <br/> |<span data-ttu-id="bde34-137">#N/A!</span><span class="sxs-lookup"><span data-stu-id="bde34-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="bde34-138">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="bde34-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="bde34-139">=ISERRNA(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="bde34-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="bde34-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="bde34-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="bde34-141">Devuelve TRUE (verdadero) ya que el valor devuelto es un error del tipo #N/A!</span><span class="sxs-lookup"><span data-stu-id="bde34-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

