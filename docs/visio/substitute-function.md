---
title: SUBSTITUTE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Reemplaza parte de una cadena de texto con una cadena de texto diferente.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 4590b7ed906d008693a58abe63f089ed8a380b34
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2018
ms.locfileid: "26643216"
---
# <a name="substitute-function"></a><span data-ttu-id="cd166-103">Función SUBSTITUTE</span><span class="sxs-lookup"><span data-stu-id="cd166-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="cd166-104">Reemplaza parte de una cadena de texto con una cadena de texto diferente.</span><span class="sxs-lookup"><span data-stu-id="cd166-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cd166-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd166-105">Syntax</span></span>

 <span data-ttu-id="cd166-106">SUBSTITUTE (\*\* *texto* \*\*, \*\* *texto_anterior* \*\*, \*\* *texto_nuevo* \*\* [, \*\* *número_inicio* \*\*] [, \*\* *distinguir_mayúsculas_minúsculas_opcional* \*\*)</span><span class="sxs-lookup"><span data-stu-id="cd166-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cd166-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd166-107">Parameters</span></span>

|<span data-ttu-id="cd166-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="cd166-108">**Name**</span></span>|<span data-ttu-id="cd166-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="cd166-109">**Required/Optional**</span></span>|<span data-ttu-id="cd166-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="cd166-110">**Data Type**</span></span>|<span data-ttu-id="cd166-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cd166-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cd166-112">_text_</span><span class="sxs-lookup"><span data-stu-id="cd166-112">_text_</span></span> <br/> |<span data-ttu-id="cd166-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd166-113">Required</span></span>  <br/> |<span data-ttu-id="cd166-114">**String**</span><span class="sxs-lookup"><span data-stu-id="cd166-114">**String**</span></span> <br/> | <span data-ttu-id="cd166-115">El texto o la referencia a la celda que contiene el texto cuyos caracteres se desea reemplazar.</span><span class="sxs-lookup"><span data-stu-id="cd166-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="cd166-116">_texto original_</span><span class="sxs-lookup"><span data-stu-id="cd166-116">_old_text_</span></span> <br/> |<span data-ttu-id="cd166-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd166-117">Required</span></span>  <br/> |<span data-ttu-id="cd166-118">**String**</span><span class="sxs-lookup"><span data-stu-id="cd166-118">**String**</span></span> <br/> | <span data-ttu-id="cd166-119">El texto que se desea reemplazar.
</span><span class="sxs-lookup"><span data-stu-id="cd166-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="cd166-120">_texto_nuevo_</span><span class="sxs-lookup"><span data-stu-id="cd166-120">_new_text_</span></span> <br/> |<span data-ttu-id="cd166-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="cd166-121">Required</span></span>  <br/> |<span data-ttu-id="cd166-122">**String**</span><span class="sxs-lookup"><span data-stu-id="cd166-122">**String**</span></span> <br/> | <span data-ttu-id="cd166-123">El texto que desea usar para reemplazar el _texto original_.</span><span class="sxs-lookup"><span data-stu-id="cd166-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="cd166-124">_número_inicio_opcional_</span><span class="sxs-lookup"><span data-stu-id="cd166-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="cd166-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="cd166-125">Optional</span></span>  <br/> |<span data-ttu-id="cd166-126">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="cd166-126">**Numeric**</span></span> <br/> |<span data-ttu-id="cd166-127">Especifica que las apariciones de texto_anterior desea reemplazar.</span><span class="sxs-lookup"><span data-stu-id="cd166-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="cd166-128">_distinguir_mayúsculas_minúsculas_opcional_</span><span class="sxs-lookup"><span data-stu-id="cd166-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="cd166-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="cd166-129">Optional</span></span>  <br/> |<span data-ttu-id="cd166-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cd166-130">**Boolean**</span></span> <br/> |<span data-ttu-id="cd166-p101">Será FALSE si diferencia entre mayúsculas y minúsculas y, si no, TRUE. El valor predeterminado es FALSE (falso).</span><span class="sxs-lookup"><span data-stu-id="cd166-p101">FALSE if case-sensitive; otherwise, TRUE. The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="cd166-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd166-133">Return value</span></span>

<span data-ttu-id="cd166-134">String</span><span class="sxs-lookup"><span data-stu-id="cd166-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cd166-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd166-135">Remarks</span></span>

 <span data-ttu-id="cd166-136">Si especifica _número_inicio_opcional_, se reemplaza la única aparición de _texto_anterior_ .</span><span class="sxs-lookup"><span data-stu-id="cd166-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="cd166-137">De lo contrario, todas las apariciones de _texto_anterior_ en _texto_ se ha cambiado a _texto_nuevo._</span><span class="sxs-lookup"><span data-stu-id="cd166-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="cd166-138">Utilice la función sustituir cuando desee reemplazar texto específico en una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="cd166-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="cd166-139">Si desea reemplazar el texto que se produce en una ubicación específica en una cadena de texto, use la función REPLACE.</span><span class="sxs-lookup"><span data-stu-id="cd166-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="cd166-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd166-140">Example</span></span>

<span data-ttu-id="cd166-141">SUBSTITUTE ("1 de enero, 2003", "de enero,", "ene")</span><span class="sxs-lookup"><span data-stu-id="cd166-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="cd166-142">Devuelve "1 ene 2003".</span><span class="sxs-lookup"><span data-stu-id="cd166-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="cd166-143">SUBSTITUTE ("1 de enero, 2003","de Enero,","ene")</span><span class="sxs-lookup"><span data-stu-id="cd166-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="cd166-144">Devuelve "1 de enero de 2003".</span><span class="sxs-lookup"><span data-stu-id="cd166-144">Returns "1 January 2003".</span></span> <span data-ttu-id="cd166-145">No hay cambios debido a que la búsqueda de texto distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cd166-145">No change is made because the text search is case-sensitive.</span></span> 
  

