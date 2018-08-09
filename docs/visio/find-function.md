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
description: Busca una cadena de texto dentro de otra cadena de texto y devuelve la posición inicial de la cadena de texto que está buscando con respecto a su posición en la cadena de texto que lo contiene.
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822167"
---
# <a name="find-function"></a><span data-ttu-id="d1406-103">Función FIND</span><span class="sxs-lookup"><span data-stu-id="d1406-103">FIND Function</span></span>

<span data-ttu-id="d1406-104">Busca una cadena de texto dentro de otra cadena de texto y devuelve la posición inicial de la cadena de texto que está buscando con respecto a su posición en la cadena de texto que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="d1406-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d1406-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1406-105">Syntax</span></span>

<span data-ttu-id="d1406-106">Buscar (** *texto_buscado* **, ** *texto_continente* **, [** *número_inicio* **], [** *no_distinguir_mayúsculas_minúsculas* **])</span><span class="sxs-lookup"><span data-stu-id="d1406-106">FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d1406-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1406-107">Parameters</span></span>

|<span data-ttu-id="d1406-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d1406-108">**Name**</span></span>|<span data-ttu-id="d1406-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="d1406-109">**Required/Optional**</span></span>|<span data-ttu-id="d1406-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="d1406-110">**Data Type**</span></span>|<span data-ttu-id="d1406-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d1406-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d1406-112">_texto buscado_</span><span class="sxs-lookup"><span data-stu-id="d1406-112">_find_text_</span></span> <br/> |<span data-ttu-id="d1406-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d1406-113">Required</span></span>  <br/> |<span data-ttu-id="d1406-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d1406-114">**String**</span></span> <br/> |<span data-ttu-id="d1406-115">El texto que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="d1406-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="d1406-116">_format_</span><span class="sxs-lookup"><span data-stu-id="d1406-116">_format_</span></span> <br/> |<span data-ttu-id="d1406-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d1406-117">Required</span></span>  <br/> |<span data-ttu-id="d1406-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d1406-118">**String**</span></span> <br/> |<span data-ttu-id="d1406-119">El texto que contiene la cadena buscada.</span><span class="sxs-lookup"><span data-stu-id="d1406-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="d1406-120">_número inicial_</span><span class="sxs-lookup"><span data-stu-id="d1406-120">_start_num_</span></span> <br/> |<span data-ttu-id="d1406-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="d1406-121">Optional</span></span>  <br/> |<span data-ttu-id="d1406-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="d1406-122">**Number**</span></span> <br/> |<span data-ttu-id="d1406-123">El carácter en el que se va a iniciar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d1406-123">The character at which to start the search.</span></span> <span data-ttu-id="d1406-124">El primer carácter de _texto_continente_ es 1.</span><span class="sxs-lookup"><span data-stu-id="d1406-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="d1406-125">Si _número_inicio_ es que faltan, se supone que es 1.</span><span class="sxs-lookup"><span data-stu-id="d1406-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="d1406-126">_no_distinguir_mayúsculas_minúsculas_</span><span class="sxs-lookup"><span data-stu-id="d1406-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="d1406-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="d1406-127">Optional</span></span>  <br/> |<span data-ttu-id="d1406-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d1406-128">**Boolean**</span></span> <br/> |<span data-ttu-id="d1406-p102">De manera predeterminada, la función FIND distingue entre mayúsculas y minúsculas. Si desea que encuentre el texto sin diferenciar entre mayúsculas y minúsculas, establezca el argumento en TRUE.</span><span class="sxs-lookup"><span data-stu-id="d1406-p102">By default, the FIND function is case-sensitive. If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d1406-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1406-131">Return value</span></span>

<span data-ttu-id="d1406-132">Number</span><span class="sxs-lookup"><span data-stu-id="d1406-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1406-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1406-133">Remarks</span></span>

<span data-ttu-id="d1406-134">Si se encuentran varias coincidencias, la función FIND devuelve la posición inicial de la primera coincidencia en la cadena.</span><span class="sxs-lookup"><span data-stu-id="d1406-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="d1406-135">El argumento de _texto buscado_ no tiene en cuenta los caracteres comodines.</span><span class="sxs-lookup"><span data-stu-id="d1406-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="d1406-136">Si _texto_buscado_:</span><span class="sxs-lookup"><span data-stu-id="d1406-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="d1406-137">Está vacío (""), FIND coincide con el primer carácter de la cadena de búsqueda (es decir, el carácter numeradas _número_inicio_ o 1).</span><span class="sxs-lookup"><span data-stu-id="d1406-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="d1406-138">¡No aparece en _texto_continente_, devolverá #VALUE!</span><span class="sxs-lookup"><span data-stu-id="d1406-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="d1406-139">valor de error.</span><span class="sxs-lookup"><span data-stu-id="d1406-139">error value.</span></span> 
    
<span data-ttu-id="d1406-140">Si _número_inicio_:</span><span class="sxs-lookup"><span data-stu-id="d1406-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="d1406-p105">No es mayor que cero (0), devolverá el error #VALUE!</span><span class="sxs-lookup"><span data-stu-id="d1406-p105">Is not greater than zero (0), FIND returns the #VALUE! error value.</span></span> 
    
- <span data-ttu-id="d1406-143">Es mayor que la longitud de _texto_continente_, devolverá #VALUE!</span><span class="sxs-lookup"><span data-stu-id="d1406-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="d1406-144">valor de error.</span><span class="sxs-lookup"><span data-stu-id="d1406-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="d1406-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d1406-145">Example</span></span>

<span data-ttu-id="d1406-146">FIND ("2003","1 de enero, 2003")</span><span class="sxs-lookup"><span data-stu-id="d1406-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="d1406-147">Devuelve 12.</span><span class="sxs-lookup"><span data-stu-id="d1406-147">Returns 12.</span></span> 
  

