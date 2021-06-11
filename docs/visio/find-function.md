---
title: FIND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Busca una cadena de texto incluida en otra cadena de texto y devuelve la posición inicial de la cadena de texto que está buscando en relación con su posición en la cadena de texto que la contiene.
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426579"
---
# <a name="find-function"></a><span data-ttu-id="4bd8a-103">Función FIND</span><span class="sxs-lookup"><span data-stu-id="4bd8a-103">FIND Function</span></span>

<span data-ttu-id="4bd8a-104">Busca una cadena de texto incluida en otra cadena de texto y devuelve la posición inicial de la cadena de texto que está buscando en relación con su posición en la cadena de texto que la contiene.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4bd8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bd8a-105">Syntax</span></span>

<span data-ttu-id="4bd8a-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="4bd8a-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4bd8a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bd8a-107">Parameters</span></span>

|<span data-ttu-id="4bd8a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4bd8a-108">**Name**</span></span>|<span data-ttu-id="4bd8a-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="4bd8a-109">**Required/Optional**</span></span>|<span data-ttu-id="4bd8a-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4bd8a-110">**Data Type**</span></span>|<span data-ttu-id="4bd8a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4bd8a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4bd8a-112">_find_text_</span><span class="sxs-lookup"><span data-stu-id="4bd8a-112">_find_text_</span></span> <br/> |<span data-ttu-id="4bd8a-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4bd8a-113">Required</span></span>  <br/> |<span data-ttu-id="4bd8a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4bd8a-114">**String**</span></span> <br/> |<span data-ttu-id="4bd8a-115">El texto que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="4bd8a-116">_format_</span><span class="sxs-lookup"><span data-stu-id="4bd8a-116">_format_</span></span> <br/> |<span data-ttu-id="4bd8a-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4bd8a-117">Required</span></span>  <br/> |<span data-ttu-id="4bd8a-118">**String**</span><span class="sxs-lookup"><span data-stu-id="4bd8a-118">**String**</span></span> <br/> |<span data-ttu-id="4bd8a-119">El texto que contiene la cadena buscada.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="4bd8a-120">_start_num_</span><span class="sxs-lookup"><span data-stu-id="4bd8a-120">_start_num_</span></span> <br/> |<span data-ttu-id="4bd8a-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="4bd8a-121">Optional</span></span>  <br/> |<span data-ttu-id="4bd8a-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="4bd8a-122">**Number**</span></span> <br/> |<span data-ttu-id="4bd8a-123">El carácter por el cual se empezará la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-123">The character at which to start the search.</span></span> <span data-ttu-id="4bd8a-124">El primer carácter de  _within_text_ es 1.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="4bd8a-125">Si  _start_num_ falta, se supone que es 1.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="4bd8a-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="4bd8a-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="4bd8a-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="4bd8a-127">Optional</span></span>  <br/> |<span data-ttu-id="4bd8a-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4bd8a-128">**Boolean**</span></span> <br/> |<span data-ttu-id="4bd8a-p102">De manera predeterminada, la función FIND distingue entre mayúsculas y minúsculas. Si desea que encuentre el texto sin diferenciar entre mayúsculas y minúsculas, establezca el argumento en TRUE.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-p102">By default, the FIND function is case-sensitive. If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4bd8a-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bd8a-131">Return value</span></span>

<span data-ttu-id="4bd8a-132">Número</span><span class="sxs-lookup"><span data-stu-id="4bd8a-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4bd8a-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4bd8a-133">Remarks</span></span>

<span data-ttu-id="4bd8a-134">Si se encuentra el texto varias veces, la función FIND devolverá la posición de inicio de la primera aparición en la cadena.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="4bd8a-135">El  _find_text_ no considera que ningún carácter sea comodín.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="4bd8a-136">Si  _find_text_:</span><span class="sxs-lookup"><span data-stu-id="4bd8a-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="4bd8a-137">Está vacío (""), FIND coincide con el primer carácter de la cadena de búsqueda (es decir, el carácter  _numerado start_num_ o 1).</span><span class="sxs-lookup"><span data-stu-id="4bd8a-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="4bd8a-138">No aparece  _en_ within_text , FIND devuelve el #VALUE!</span><span class="sxs-lookup"><span data-stu-id="4bd8a-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="4bd8a-139">valor de error.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-139">error value.</span></span> 
    
<span data-ttu-id="4bd8a-140">Si  _start_num_:</span><span class="sxs-lookup"><span data-stu-id="4bd8a-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="4bd8a-p105">No es mayor que cero (0), devolverá el error #VALUE!</span><span class="sxs-lookup"><span data-stu-id="4bd8a-p105">Is not greater than zero (0), FIND returns the #VALUE! error value.</span></span> 
    
- <span data-ttu-id="4bd8a-143">Es mayor que la longitud de  _within_text_, FINDreturns el #VALUE!</span><span class="sxs-lookup"><span data-stu-id="4bd8a-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="4bd8a-144">valor de error.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="4bd8a-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4bd8a-145">Example</span></span>

<span data-ttu-id="4bd8a-146">FIND ("2003","1 de enero, 2003")</span><span class="sxs-lookup"><span data-stu-id="4bd8a-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="4bd8a-147">Devuelve 12.</span><span class="sxs-lookup"><span data-stu-id="4bd8a-147">Returns 12.</span></span> 
  

