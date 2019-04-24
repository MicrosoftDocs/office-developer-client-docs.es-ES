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
description: Busca una cadena de texto contenida en otra cadena de texto y devuelve la posición inicial de la cadena de texto que está buscando en relación con su posición en la cadena de texto que la contiene.
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322501"
---
# <a name="find-function"></a><span data-ttu-id="df9ac-103">Función FIND</span><span class="sxs-lookup"><span data-stu-id="df9ac-103">FIND Function</span></span>

<span data-ttu-id="df9ac-104">Busca una cadena de texto contenida en otra cadena de texto y devuelve la posición inicial de la cadena de texto que está buscando en relación con su posición en la cadena de texto que la contiene.</span><span class="sxs-lookup"><span data-stu-id="df9ac-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="df9ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df9ac-105">Syntax</span></span>

<span data-ttu-id="df9ac-106">Find (\* \* *texto_buscado* \* \*, \* \* *dentro_del_texto* \* *, [* \* *núm_inicial* \* *], [* \* *ignore_case* \* \*])</span><span class="sxs-lookup"><span data-stu-id="df9ac-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="df9ac-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df9ac-107">Parameters</span></span>

|<span data-ttu-id="df9ac-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="df9ac-108">**Name**</span></span>|<span data-ttu-id="df9ac-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="df9ac-109">**Required/Optional**</span></span>|<span data-ttu-id="df9ac-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="df9ac-110">**Data Type**</span></span>|<span data-ttu-id="df9ac-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df9ac-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="df9ac-112">_texto_buscado_</span><span class="sxs-lookup"><span data-stu-id="df9ac-112">_find_text_</span></span> <br/> |<span data-ttu-id="df9ac-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="df9ac-113">Required</span></span>  <br/> |<span data-ttu-id="df9ac-114">**String**</span><span class="sxs-lookup"><span data-stu-id="df9ac-114">**String**</span></span> <br/> |<span data-ttu-id="df9ac-115">El texto que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="df9ac-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="df9ac-116">_format_</span><span class="sxs-lookup"><span data-stu-id="df9ac-116">_format_</span></span> <br/> |<span data-ttu-id="df9ac-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="df9ac-117">Required</span></span>  <br/> |<span data-ttu-id="df9ac-118">**String**</span><span class="sxs-lookup"><span data-stu-id="df9ac-118">**String**</span></span> <br/> |<span data-ttu-id="df9ac-119">El texto que contiene la cadena buscada.</span><span class="sxs-lookup"><span data-stu-id="df9ac-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="df9ac-120">_Núm_inicial_</span><span class="sxs-lookup"><span data-stu-id="df9ac-120">_start_num_</span></span> <br/> |<span data-ttu-id="df9ac-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="df9ac-121">Optional</span></span>  <br/> |<span data-ttu-id="df9ac-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="df9ac-122">**Number**</span></span> <br/> |<span data-ttu-id="df9ac-123">El carácter por el cual se empezará la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="df9ac-123">The character at which to start the search.</span></span> <span data-ttu-id="df9ac-124">El primer carácter de _dentro_del_texto_ es 1.</span><span class="sxs-lookup"><span data-stu-id="df9ac-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="df9ac-125">Si no se encuentra _núm_inicial_ , se supone que es 1.</span><span class="sxs-lookup"><span data-stu-id="df9ac-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="df9ac-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="df9ac-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="df9ac-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="df9ac-127">Optional</span></span>  <br/> |<span data-ttu-id="df9ac-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="df9ac-128">**Boolean**</span></span> <br/> |<span data-ttu-id="df9ac-129">De manera predeterminada, la función FIND distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="df9ac-129">By default, the FIND function is case-sensitive.</span></span> <span data-ttu-id="df9ac-130">Si desea que encuentre el texto sin diferenciar entre mayúsculas y minúsculas, establezca el argumento en TRUE.</span><span class="sxs-lookup"><span data-stu-id="df9ac-130">If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="df9ac-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df9ac-131">Return value</span></span>

<span data-ttu-id="df9ac-132">Número</span><span class="sxs-lookup"><span data-stu-id="df9ac-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df9ac-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df9ac-133">Remarks</span></span>

<span data-ttu-id="df9ac-134">Si se encuentra el texto varias veces, la función FIND devolverá la posición de inicio de la primera aparición en la cadena.</span><span class="sxs-lookup"><span data-stu-id="df9ac-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="df9ac-135">El argumento _texto_buscado_ no tiene en cuenta los caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="df9ac-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="df9ac-136">Si _texto_buscado_:</span><span class="sxs-lookup"><span data-stu-id="df9ac-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="df9ac-137">Está vacío (""), FIND coincide con el primer carácter de la cadena de búsqueda (es decir, el carácter con el número _núm_inicial_ o 1).</span><span class="sxs-lookup"><span data-stu-id="df9ac-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="df9ac-138">No aparece en _dentro_del_texto_, Find devuelve el #VALUE!</span><span class="sxs-lookup"><span data-stu-id="df9ac-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="df9ac-139">valor de error.</span><span class="sxs-lookup"><span data-stu-id="df9ac-139">error value.</span></span> 
    
<span data-ttu-id="df9ac-140">Si _núm_inicial_:</span><span class="sxs-lookup"><span data-stu-id="df9ac-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="df9ac-141">No es mayor que cero (0), FIND devuelve el #VALUE!</span><span class="sxs-lookup"><span data-stu-id="df9ac-141">Is not greater than zero (0), FIND returns the #VALUE!</span></span> <span data-ttu-id="df9ac-142">valor de error.</span><span class="sxs-lookup"><span data-stu-id="df9ac-142">error value.</span></span> 
    
- <span data-ttu-id="df9ac-143">Es mayor que la longitud de _dentro_del_texto_, devolverá el #VALUE!</span><span class="sxs-lookup"><span data-stu-id="df9ac-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="df9ac-144">valor de error.</span><span class="sxs-lookup"><span data-stu-id="df9ac-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="df9ac-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df9ac-145">Example</span></span>

<span data-ttu-id="df9ac-146">FIND ("2003","1 de enero, 2003")</span><span class="sxs-lookup"><span data-stu-id="df9ac-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="df9ac-147">Devuelve 12.</span><span class="sxs-lookup"><span data-stu-id="df9ac-147">Returns 12.</span></span> 
  

