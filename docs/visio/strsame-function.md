---
title: STRSAME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Determina si las cadenas son los mismos. Devuelve TRUE si son iguales y FALSE si no lo son.
ms.openlocfilehash: 5365ce6e679f708a47f4bcbdebbc4cabb13a2aee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823321"
---
# <a name="strsame-function"></a><span data-ttu-id="9c0c5-104">Función STRSAME</span><span class="sxs-lookup"><span data-stu-id="9c0c5-104">STRSAME Function</span></span>

<span data-ttu-id="9c0c5-105">Determina si las cadenas son los mismos.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-105">Determines whether strings are the same.</span></span> <span data-ttu-id="9c0c5-106">Devuelve TRUE si son iguales y FALSE si no lo son.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-106">It returns TRUE if they are the same and FALSE if they aren't.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9c0c5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c0c5-107">Syntax</span></span>

<span data-ttu-id="9c0c5-108">STRSAME ("** *cadena1* **","** *cadena2* **", ** *ignoreCase* **)</span><span class="sxs-lookup"><span data-stu-id="9c0c5-108">STRSAME (" ** *string1* ** ", " ** *string2* ** ", ** *ignoreCase* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9c0c5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c0c5-109">Parameters</span></span>

|<span data-ttu-id="9c0c5-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="9c0c5-110">**Name**</span></span>|<span data-ttu-id="9c0c5-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="9c0c5-111">**Required/Optional**</span></span>|<span data-ttu-id="9c0c5-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="9c0c5-112">**Data Type**</span></span>|<span data-ttu-id="9c0c5-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9c0c5-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9c0c5-114">_cadena1_</span><span class="sxs-lookup"><span data-stu-id="9c0c5-114">_string1_</span></span> <br/> |<span data-ttu-id="9c0c5-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9c0c5-115">Required</span></span>  <br/> |<span data-ttu-id="9c0c5-116">**String**</span><span class="sxs-lookup"><span data-stu-id="9c0c5-116">**String**</span></span> <br/> |<span data-ttu-id="9c0c5-117">La primera cadena de la comparación.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-117">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="9c0c5-118">_cadena2_</span><span class="sxs-lookup"><span data-stu-id="9c0c5-118">_string2_</span></span> <br/> |<span data-ttu-id="9c0c5-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9c0c5-119">Required</span></span>  <br/> |<span data-ttu-id="9c0c5-120">**String**</span><span class="sxs-lookup"><span data-stu-id="9c0c5-120">**String**</span></span> <br/> |<span data-ttu-id="9c0c5-121">La segunda cadena de la comparación.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-121">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="9c0c5-122">_ignoreCase_</span><span class="sxs-lookup"><span data-stu-id="9c0c5-122">_ignoreCase_</span></span> <br/> |<span data-ttu-id="9c0c5-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="9c0c5-123">Optional</span></span>  <br/> |<span data-ttu-id="9c0c5-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9c0c5-124">**Boolean**</span></span> <br/> |<span data-ttu-id="9c0c5-p103">TRUE (verdadero) para no distinguir mayúsculas y minúsculas y FALSE (falso) para hacerlo. El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-p103">TRUE to ignore the case and FALSE to compare the case. The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9c0c5-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c0c5-127">Return value</span></span>

<span data-ttu-id="9c0c5-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="9c0c5-128">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c0c5-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c0c5-129">Remarks</span></span>

<span data-ttu-id="9c0c5-130">Para comparar cadenas de varios bytes o para hacer comparaciones utilizando reglas para una configuración local específica, use la función STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-130">To compare multi-byte strings or to do comparisons using case rules for a specific locale, use the STRSAMEEX function.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="9c0c5-131">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c0c5-131">Example 1</span></span>

<span data-ttu-id="9c0c5-132">STRSAME("gato","perro")</span><span class="sxs-lookup"><span data-stu-id="9c0c5-132">STRSAME("cat","dog")</span></span>
  
<span data-ttu-id="9c0c5-133">Devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-133">Returns FALSE.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9c0c5-134">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="9c0c5-134">Example 2</span></span>

<span data-ttu-id="9c0c5-135">STRSAME("gato","gato")</span><span class="sxs-lookup"><span data-stu-id="9c0c5-135">STRSAME("cat","cat")</span></span>
  
<span data-ttu-id="9c0c5-136">Devuelve TRUE.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-136">Returns TRUE.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="9c0c5-137">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="9c0c5-137">Example 3</span></span>

<span data-ttu-id="9c0c5-138">STRSAME("gato","gato", TRUE)</span><span class="sxs-lookup"><span data-stu-id="9c0c5-138">STRSAME("cat","cat", TRUE)</span></span>
  
<span data-ttu-id="9c0c5-139">Devuelve TRUE.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-139">Returns TRUE.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="9c0c5-140">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="9c0c5-140">Example 4</span></span>

<span data-ttu-id="9c0c5-141">STRSAME("gato","GATO")</span><span class="sxs-lookup"><span data-stu-id="9c0c5-141">STRSAME("cat","CAT")</span></span>
  
<span data-ttu-id="9c0c5-142">Devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-142">Returns FALSE.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="9c0c5-143">Ejemplo 5</span><span class="sxs-lookup"><span data-stu-id="9c0c5-143">Example 5</span></span>

<span data-ttu-id="9c0c5-144">STRSAME("gato","GATO", TRUE)</span><span class="sxs-lookup"><span data-stu-id="9c0c5-144">STRSAME("cat","CAT", TRUE)</span></span>
  
<span data-ttu-id="9c0c5-145">Devuelve TRUE.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-145">Returns TRUE.</span></span>
  
## <a name="example-6"></a><span data-ttu-id="9c0c5-146">Ejemplo 6</span><span class="sxs-lookup"><span data-stu-id="9c0c5-146">Example 6</span></span>

<span data-ttu-id="9c0c5-147">STRSAME("gäto,"GATO", TRUE)</span><span class="sxs-lookup"><span data-stu-id="9c0c5-147">STRSAME("cät,"CAT", TRUE)</span></span>
  
<span data-ttu-id="9c0c5-148">Devuelve FALSE.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-148">Returns FALSE.</span></span>
  
## <a name="example-7"></a><span data-ttu-id="9c0c5-149">Ejemplo 7</span><span class="sxs-lookup"><span data-stu-id="9c0c5-149">Example 7</span></span>

<span data-ttu-id="9c0c5-150">STRSAME("gäto,"GÄTO", TRUE)</span><span class="sxs-lookup"><span data-stu-id="9c0c5-150">STRSAME("cät,"CÄT", TRUE)</span></span>
  
<span data-ttu-id="9c0c5-151">Devuelve TRUE.</span><span class="sxs-lookup"><span data-stu-id="9c0c5-151">Returns TRUE.</span></span>
  

