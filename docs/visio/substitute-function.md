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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346826"
---
# <a name="substitute-function"></a><span data-ttu-id="df7b5-103">Función SUBSTITUTE</span><span class="sxs-lookup"><span data-stu-id="df7b5-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="df7b5-104">Reemplaza parte de una cadena de texto con una cadena de texto diferente.</span><span class="sxs-lookup"><span data-stu-id="df7b5-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="df7b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df7b5-105">Syntax</span></span>

 <span data-ttu-id="df7b5-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span><span class="sxs-lookup"><span data-stu-id="df7b5-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="df7b5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df7b5-107">Parameters</span></span>

|<span data-ttu-id="df7b5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="df7b5-108">**Name**</span></span>|<span data-ttu-id="df7b5-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="df7b5-109">**Required/Optional**</span></span>|<span data-ttu-id="df7b5-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="df7b5-110">**Data Type**</span></span>|<span data-ttu-id="df7b5-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df7b5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="df7b5-112">_text_</span><span class="sxs-lookup"><span data-stu-id="df7b5-112">_text_</span></span> <br/> |<span data-ttu-id="df7b5-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="df7b5-113">Required</span></span>  <br/> |<span data-ttu-id="df7b5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="df7b5-114">**String**</span></span> <br/> | <span data-ttu-id="df7b5-115">El texto o la referencia a la celda que contiene el texto cuyos caracteres se desea reemplazar.</span><span class="sxs-lookup"><span data-stu-id="df7b5-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="df7b5-116">_old_text_</span><span class="sxs-lookup"><span data-stu-id="df7b5-116">_old_text_</span></span> <br/> |<span data-ttu-id="df7b5-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="df7b5-117">Required</span></span>  <br/> |<span data-ttu-id="df7b5-118">**String**</span><span class="sxs-lookup"><span data-stu-id="df7b5-118">**String**</span></span> <br/> | <span data-ttu-id="df7b5-119">El texto que se desea reemplazar.</span><span class="sxs-lookup"><span data-stu-id="df7b5-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="df7b5-120">_new_text_</span><span class="sxs-lookup"><span data-stu-id="df7b5-120">_new_text_</span></span> <br/> |<span data-ttu-id="df7b5-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="df7b5-121">Required</span></span>  <br/> |<span data-ttu-id="df7b5-122">**String**</span><span class="sxs-lookup"><span data-stu-id="df7b5-122">**String**</span></span> <br/> | <span data-ttu-id="df7b5-123">El texto que desea usar para  _reemplazar_ old_text .</span><span class="sxs-lookup"><span data-stu-id="df7b5-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="df7b5-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="df7b5-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="df7b5-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="df7b5-125">Optional</span></span>  <br/> |<span data-ttu-id="df7b5-126">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="df7b5-126">**Numeric**</span></span> <br/> |<span data-ttu-id="df7b5-127">Especifica qué repeticiones de old_text reemplazar.</span><span class="sxs-lookup"><span data-stu-id="df7b5-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="df7b5-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="df7b5-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="df7b5-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="df7b5-129">Optional</span></span>  <br/> |<span data-ttu-id="df7b5-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="df7b5-130">**Boolean**</span></span> <br/> |<span data-ttu-id="df7b5-131">Será FALSE si diferencia entre mayúsculas y minúsculas y, si no, TRUE.</span><span class="sxs-lookup"><span data-stu-id="df7b5-131">FALSE if case-sensitive; otherwise, TRUE.</span></span> <span data-ttu-id="df7b5-132">El valor predeterminado es FALSE (falso).</span><span class="sxs-lookup"><span data-stu-id="df7b5-132">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="df7b5-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df7b5-133">Return value</span></span>

<span data-ttu-id="df7b5-134">String</span><span class="sxs-lookup"><span data-stu-id="df7b5-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df7b5-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df7b5-135">Remarks</span></span>

 <span data-ttu-id="df7b5-136">Si especifica una  _start_num_opt_, solo se reemplaza la  _aparición old_text_ del usuario.</span><span class="sxs-lookup"><span data-stu-id="df7b5-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="df7b5-137">De lo contrario, todas  _las old_text_  _del_ texto se cambian  _a new_text._</span><span class="sxs-lookup"><span data-stu-id="df7b5-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="df7b5-138">Use esta función cuando desee reemplazar un texto específico dentro de una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="df7b5-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="df7b5-139">Si desea reemplazar texto que se produce en una ubicación específica de una cadena de texto, use la función REPLACE.</span><span class="sxs-lookup"><span data-stu-id="df7b5-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="df7b5-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df7b5-140">Example</span></span>

<span data-ttu-id="df7b5-141">SUBSTITUTE ("1 de enero, 2003", "de enero,", "ene")</span><span class="sxs-lookup"><span data-stu-id="df7b5-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="df7b5-142">Devuelve "1 ene 2003".</span><span class="sxs-lookup"><span data-stu-id="df7b5-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="df7b5-143">SUBSTITUTE ("1 de enero, 2003","de Enero,","ene")</span><span class="sxs-lookup"><span data-stu-id="df7b5-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="df7b5-144">Devuelve "1 de enero, 2003".</span><span class="sxs-lookup"><span data-stu-id="df7b5-144">Returns "1 January 2003".</span></span> <span data-ttu-id="df7b5-145">No se modifica la cadena porque la búsqueda distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="df7b5-145">No change is made because the text search is case-sensitive.</span></span> 
  

