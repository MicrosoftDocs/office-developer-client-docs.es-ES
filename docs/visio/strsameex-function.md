---
title: STRSAMEEX (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Determina si dos cadenas son los mismos.
ms.openlocfilehash: 129c7429fbb3b3e5d09193b8be570045d43a0f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823343"
---
# <a name="strsameex-function"></a><span data-ttu-id="c9109-103">STRSAMEEX (función)</span><span class="sxs-lookup"><span data-stu-id="c9109-103">STRSAMEEX Function</span></span>

<span data-ttu-id="c9109-104">Determina si dos cadenas son los mismos.</span><span class="sxs-lookup"><span data-stu-id="c9109-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c9109-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9109-105">Syntax</span></span>

<span data-ttu-id="c9109-106">STRSAMEEX ("** *cadena1* **","** *cadena2* **", ** *localeID* **, ** *marca* **)</span><span class="sxs-lookup"><span data-stu-id="c9109-106">STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c9109-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9109-107">Parameters</span></span>

|<span data-ttu-id="c9109-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c9109-108">**Name**</span></span>|<span data-ttu-id="c9109-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="c9109-109">**Required/Optional**</span></span>|<span data-ttu-id="c9109-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c9109-110">**Data Type**</span></span>|<span data-ttu-id="c9109-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9109-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c9109-112">_cadena1_</span><span class="sxs-lookup"><span data-stu-id="c9109-112">_string1_</span></span> <br/> |<span data-ttu-id="c9109-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c9109-113">Required</span></span>  <br/> |<span data-ttu-id="c9109-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c9109-114">**String**</span></span> <br/> |<span data-ttu-id="c9109-115">La primera cadena de la comparación.</span><span class="sxs-lookup"><span data-stu-id="c9109-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="c9109-116">_cadena2_</span><span class="sxs-lookup"><span data-stu-id="c9109-116">_string2_</span></span> <br/> |<span data-ttu-id="c9109-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c9109-117">Required</span></span>  <br/> |<span data-ttu-id="c9109-118">**String**</span><span class="sxs-lookup"><span data-stu-id="c9109-118">**String**</span></span> <br/> | <span data-ttu-id="c9109-119">La segunda cadena de la comparación.</span><span class="sxs-lookup"><span data-stu-id="c9109-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="c9109-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="c9109-120">_localeID_</span></span> <br/> |<span data-ttu-id="c9109-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c9109-121">Required</span></span>  <br/> |<span data-ttu-id="c9109-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="c9109-122">**Numeric**</span></span> <br/> |<span data-ttu-id="c9109-123">El código del identificador regional.</span><span class="sxs-lookup"><span data-stu-id="c9109-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="c9109-124">_marca_</span><span class="sxs-lookup"><span data-stu-id="c9109-124">_flag_</span></span> <br/> |<span data-ttu-id="c9109-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c9109-125">Required</span></span>  <br/> |<span data-ttu-id="c9109-126">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="c9109-126">**Numeric**</span></span> <br/> | <span data-ttu-id="c9109-127">Un bit que especifica el tipo de comparación.</span><span class="sxs-lookup"><span data-stu-id="c9109-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c9109-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9109-128">Return value</span></span>

<span data-ttu-id="c9109-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="c9109-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c9109-130">Notas</span><span class="sxs-lookup"><span data-stu-id="c9109-130">Remarks</span></span>

<span data-ttu-id="c9109-131">STRSAMEEX devuelve TRUE si ambas cadenas de entrada son los mismos y FALSE si no lo son.</span><span class="sxs-lookup"><span data-stu-id="c9109-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="c9109-132">Utilice esta función para comparar cadenas de varios bytes o para hacer comparaciones que usan las reglas de mayúsculas y minúsculas para una configuración regional específica.</span><span class="sxs-lookup"><span data-stu-id="c9109-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="c9109-133">En la función STRSAMEEX, puede usar cualquier combinación de las siguientes marcas.</span><span class="sxs-lookup"><span data-stu-id="c9109-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="c9109-134">**Flag**</span><span class="sxs-lookup"><span data-stu-id="c9109-134">**Flag**</span></span>|<span data-ttu-id="c9109-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9109-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c9109-136">1</span><span class="sxs-lookup"><span data-stu-id="c9109-136">1</span></span>  <br/> |<span data-ttu-id="c9109-137">No distinguir mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c9109-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="c9109-138">2</span><span class="sxs-lookup"><span data-stu-id="c9109-138">2</span></span>  <br/> |<span data-ttu-id="c9109-139">Omitir los caracteres que no ocupan un espacio.</span><span class="sxs-lookup"><span data-stu-id="c9109-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="c9109-140">4</span><span class="sxs-lookup"><span data-stu-id="c9109-140">4</span></span>  <br/> |<span data-ttu-id="c9109-141">Omitir los símbolos.</span><span class="sxs-lookup"><span data-stu-id="c9109-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="c9109-142">4096</span><span class="sxs-lookup"><span data-stu-id="c9109-142">4096</span></span>  <br/> |<span data-ttu-id="c9109-143">Tratar la puntuación igual que los símbolos.</span><span class="sxs-lookup"><span data-stu-id="c9109-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="c9109-144">65536</span><span class="sxs-lookup"><span data-stu-id="c9109-144">65536</span></span>  <br/> |<span data-ttu-id="c9109-145">No distinguir entre caracteres Hiragana y Katakana.</span><span class="sxs-lookup"><span data-stu-id="c9109-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="c9109-146">131072</span><span class="sxs-lookup"><span data-stu-id="c9109-146">131072</span></span>  <br/> |<span data-ttu-id="c9109-147">No distinguir entre un carácter de un byte y el mismo como carácter de doble byte.</span><span class="sxs-lookup"><span data-stu-id="c9109-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

