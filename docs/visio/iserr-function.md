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
description: 'Devuelve TRUE si el valor de referenciaDeCelda es algún tipo de error excepto # n/a; de lo contrario, devuelve FALSE. La función ISERR se utiliza en fórmulas que hacen referencia a otra celda.'
ms.openlocfilehash: 651b095e53b7f2690aa9c8774d87d5afcede75be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822360"
---
# <a name="iserr-function"></a><span data-ttu-id="5c319-104">Función ISERR</span><span class="sxs-lookup"><span data-stu-id="5c319-104">ISERR Function</span></span>

<span data-ttu-id="5c319-105">Devuelve TRUE si el valor de _referenciaDeCelda_ es algún tipo de error excepto # n/a; de lo contrario, devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="5c319-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="5c319-106">La función ISERR se utiliza en fórmulas que hacen referencia a otra celda.</span><span class="sxs-lookup"><span data-stu-id="5c319-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5c319-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c319-107">Syntax</span></span>

<span data-ttu-id="5c319-108">ISERR (** *referenciaDeCelda* **)</span><span class="sxs-lookup"><span data-stu-id="5c319-108">ISERR(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5c319-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c319-109">Parameters</span></span>

|<span data-ttu-id="5c319-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5c319-110">**Name**</span></span>|<span data-ttu-id="5c319-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="5c319-111">**Required/Optional**</span></span>|<span data-ttu-id="5c319-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5c319-112">**Data Type**</span></span>|<span data-ttu-id="5c319-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c319-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5c319-114">_referenciaDeCelda_</span><span class="sxs-lookup"><span data-stu-id="5c319-114">_cellreference_</span></span> <br/> |<span data-ttu-id="5c319-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c319-115">Required</span></span>  <br/> |<span data-ttu-id="5c319-116">**String**</span><span class="sxs-lookup"><span data-stu-id="5c319-116">**String**</span></span> <br/> |<span data-ttu-id="5c319-117">Referencia a una celda.</span><span class="sxs-lookup"><span data-stu-id="5c319-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="5c319-118">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c319-118">Example 1</span></span>

|<span data-ttu-id="5c319-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="5c319-119">**Cell**</span></span>|<span data-ttu-id="5c319-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="5c319-120">**Formula**</span></span>|<span data-ttu-id="5c319-121">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="5c319-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5c319-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="5c319-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="5c319-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="5c319-123">=NA( )</span></span>  <br/> |<span data-ttu-id="5c319-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="5c319-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="5c319-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="5c319-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="5c319-126">=ISERR(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="5c319-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="5c319-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="5c319-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="5c319-p103">Devuelve FALSE ya que #N/A! es un error que la función ISERR no reconoce. Utilice ISERROR para encontrar todos los tipos de errores.</span><span class="sxs-lookup"><span data-stu-id="5c319-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5c319-131">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="5c319-131">Example 2</span></span>

|<span data-ttu-id="5c319-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="5c319-132">**Cell**</span></span>|<span data-ttu-id="5c319-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="5c319-133">**Formula**</span></span>|<span data-ttu-id="5c319-134">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="5c319-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5c319-135">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="5c319-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="5c319-136">="Casa"</span><span class="sxs-lookup"><span data-stu-id="5c319-136">="House"</span></span>  <br/> |<span data-ttu-id="5c319-137">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="5c319-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="5c319-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="5c319-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="5c319-139">=ISERR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="5c319-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="5c319-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="5c319-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="5c319-p104">Devuelve TRUE ya que #VALUE! es un error que la función ISERR reconoce.</span><span class="sxs-lookup"><span data-stu-id="5c319-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

