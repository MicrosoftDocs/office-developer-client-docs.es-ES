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
description: Determina si dos cadenas son iguales.
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329795"
---
# <a name="strsameex-function"></a><span data-ttu-id="6dfaa-103">Función STRSAMEEX</span><span class="sxs-lookup"><span data-stu-id="6dfaa-103">STRSAMEEX Function</span></span>

<span data-ttu-id="6dfaa-104">Determina si dos cadenas son iguales.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6dfaa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6dfaa-105">Syntax</span></span>

<span data-ttu-id="6dfaa-106">STRSAMEEX ("\* \* *string1* \* *", "* \* *cadena2* \* \*", \* \* *localeID* \* \*, \* \* *Flag* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6dfaa-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6dfaa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6dfaa-107">Parameters</span></span>

|<span data-ttu-id="6dfaa-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6dfaa-108">**Name**</span></span>|<span data-ttu-id="6dfaa-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="6dfaa-109">**Required/Optional**</span></span>|<span data-ttu-id="6dfaa-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="6dfaa-110">**Data Type**</span></span>|<span data-ttu-id="6dfaa-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6dfaa-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6dfaa-112">_string1_</span><span class="sxs-lookup"><span data-stu-id="6dfaa-112">_string1_</span></span> <br/> |<span data-ttu-id="6dfaa-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6dfaa-113">Required</span></span>  <br/> |<span data-ttu-id="6dfaa-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6dfaa-114">**String**</span></span> <br/> |<span data-ttu-id="6dfaa-115">La primera cadena de la comparación.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="6dfaa-116">_string2_</span><span class="sxs-lookup"><span data-stu-id="6dfaa-116">_string2_</span></span> <br/> |<span data-ttu-id="6dfaa-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6dfaa-117">Required</span></span>  <br/> |<span data-ttu-id="6dfaa-118">**String**</span><span class="sxs-lookup"><span data-stu-id="6dfaa-118">**String**</span></span> <br/> | <span data-ttu-id="6dfaa-119">La segunda cadena de la comparación.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="6dfaa-120">_Regional_</span><span class="sxs-lookup"><span data-stu-id="6dfaa-120">_localeID_</span></span> <br/> |<span data-ttu-id="6dfaa-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6dfaa-121">Required</span></span>  <br/> |<span data-ttu-id="6dfaa-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="6dfaa-122">**Numeric**</span></span> <br/> |<span data-ttu-id="6dfaa-123">El código del identificador regional.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="6dfaa-124">_flag_</span><span class="sxs-lookup"><span data-stu-id="6dfaa-124">_flag_</span></span> <br/> |<span data-ttu-id="6dfaa-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6dfaa-125">Required</span></span>  <br/> |<span data-ttu-id="6dfaa-126">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="6dfaa-126">**Numeric**</span></span> <br/> | <span data-ttu-id="6dfaa-127">Un bit que especifica el tipo de comparación.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6dfaa-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6dfaa-128">Return value</span></span>

<span data-ttu-id="6dfaa-129">Booleano</span><span class="sxs-lookup"><span data-stu-id="6dfaa-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6dfaa-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6dfaa-130">Remarks</span></span>

<span data-ttu-id="6dfaa-131">STRSAMEEX devuelve TRUE (verdadero) si son iguales y FALSE (falso) si no lo son.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="6dfaa-132">Use esta función para comparar cadenas de varios bytes o para hacer comparaciones usando reglas para una configuración local específica.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="6dfaa-133">En la función STRSAMEEX, puede usar cualquier combinación de las siguientes marcas.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="6dfaa-134">**Flag**</span><span class="sxs-lookup"><span data-stu-id="6dfaa-134">**Flag**</span></span>|<span data-ttu-id="6dfaa-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6dfaa-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6dfaa-136">1</span><span class="sxs-lookup"><span data-stu-id="6dfaa-136">1</span></span>  <br/> |<span data-ttu-id="6dfaa-137">No distinguir mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="6dfaa-138">segundo</span><span class="sxs-lookup"><span data-stu-id="6dfaa-138">2</span></span>  <br/> |<span data-ttu-id="6dfaa-139">Omitir los caracteres que no ocupan un espacio.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="6dfaa-140">4</span><span class="sxs-lookup"><span data-stu-id="6dfaa-140">4</span></span>  <br/> |<span data-ttu-id="6dfaa-141">Omitir los símbolos.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="6dfaa-142">4096</span><span class="sxs-lookup"><span data-stu-id="6dfaa-142">4096</span></span>  <br/> |<span data-ttu-id="6dfaa-143">Tratar la puntuación igual que los símbolos.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="6dfaa-144">65536</span><span class="sxs-lookup"><span data-stu-id="6dfaa-144">65536</span></span>  <br/> |<span data-ttu-id="6dfaa-145">No distinguir entre caracteres Hiragana y Katakana.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="6dfaa-146">131072</span><span class="sxs-lookup"><span data-stu-id="6dfaa-146">131072</span></span>  <br/> |<span data-ttu-id="6dfaa-147">No distinguir entre un carácter de un byte y el mismo como carácter de doble byte.</span><span class="sxs-lookup"><span data-stu-id="6dfaa-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

