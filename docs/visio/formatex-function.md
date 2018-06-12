---
title: FORMATEX (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
localization_priority: Normal
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: Devuelve el resultado de expresión evaluado en unidadesDeOrigen como una cadena con formato de acuerdo con el formato expresado en unidadesDeDestino.
ms.openlocfilehash: 08d123967272e0ab4e25990bcfab55cc80cef55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822200"
---
# <a name="formatex-function"></a><span data-ttu-id="130d4-103">FORMATEX (función)</span><span class="sxs-lookup"><span data-stu-id="130d4-103">FORMATEX Function</span></span>

<span data-ttu-id="130d4-104">Devuelve el resultado de expresión evaluado en unidadesDeOrigen como una cadena con formato de acuerdo con el formato expresado en unidadesDeDestino.</span><span class="sxs-lookup"><span data-stu-id="130d4-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="130d4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="130d4-105">Syntax</span></span>

<span data-ttu-id="130d4-106">FORMATEX (** *expresión* **, "** *formato* **", [** *unidadesDeOrigen* **], [** *unidadesDeDestino* **], [** *langID* **] [, ** *IDcalendario* **])</span><span class="sxs-lookup"><span data-stu-id="130d4-106">FORMATEX(** *expression* **," ** *format* ** ",[ ** *srcUnit* ** ],[ ** *dstUnit* ** ],[ ** *langID* ** ][, ** *calID* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="130d4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="130d4-107">Parameters</span></span>

|<span data-ttu-id="130d4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="130d4-108">**Name**</span></span>|<span data-ttu-id="130d4-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="130d4-109">**Required/Optional**</span></span>|<span data-ttu-id="130d4-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="130d4-110">**Data Type**</span></span>|<span data-ttu-id="130d4-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="130d4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="130d4-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="130d4-112">_expression_</span></span> <br/> |<span data-ttu-id="130d4-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="130d4-113">Required</span></span>  <br/> |<span data-ttu-id="130d4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="130d4-114">**String**</span></span> <br/> |<span data-ttu-id="130d4-115">Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor.</span><span class="sxs-lookup"><span data-stu-id="130d4-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="130d4-116">_format_</span><span class="sxs-lookup"><span data-stu-id="130d4-116">_format_</span></span> <br/> |<span data-ttu-id="130d4-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="130d4-117">Required</span></span>  <br/> |<span data-ttu-id="130d4-118">**String**</span><span class="sxs-lookup"><span data-stu-id="130d4-118">**String**</span></span> <br/> |<span data-ttu-id="130d4-119">La imagen de formato utilizada para dar formato a la cadena.</span><span class="sxs-lookup"><span data-stu-id="130d4-119">The format picture used to format the string.</span></span> <span data-ttu-id="130d4-120">Para obtener más información acerca de las imágenes de formato, vea [Acerca de las imágenes de formato](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="130d4-120">For more information about format pictures, see [About Format Pictures](about-format-pictures.md).</span></span>  <br/> |
| <span data-ttu-id="130d4-121">_unidadesDeOrigen_</span><span class="sxs-lookup"><span data-stu-id="130d4-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="130d4-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="130d4-122">Optional</span></span>  <br/> |<span data-ttu-id="130d4-123">**String**</span><span class="sxs-lookup"><span data-stu-id="130d4-123">**String**</span></span> <br/> | <span data-ttu-id="130d4-124">Unidades usadas para evaluar expresión (PDA, cm etc.).</span><span class="sxs-lookup"><span data-stu-id="130d4-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="130d4-125">_unidadesDeDestino_</span><span class="sxs-lookup"><span data-stu-id="130d4-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="130d4-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="130d4-126">Optional</span></span>  <br/> |<span data-ttu-id="130d4-127">**String**</span><span class="sxs-lookup"><span data-stu-id="130d4-127">**String**</span></span> <br/> |<span data-ttu-id="130d4-128">Unidades que se usará para el resultado de expresión (PDA, cm etc.).</span><span class="sxs-lookup"><span data-stu-id="130d4-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="130d4-129">_langID_</span><span class="sxs-lookup"><span data-stu-id="130d4-129">_langID_</span></span> <br/> |<span data-ttu-id="130d4-130">Opcional</span><span class="sxs-lookup"><span data-stu-id="130d4-130">Optional</span></span>  <br/> |<span data-ttu-id="130d4-131">**Número**</span><span class="sxs-lookup"><span data-stu-id="130d4-131">**Number**</span></span> <br/> |<span data-ttu-id="130d4-132">El idioma utilizado para dar formato a las imágenes de fecha y hora de Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="130d4-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="130d4-133">_IDcalendario_</span><span class="sxs-lookup"><span data-stu-id="130d4-133">_calID_</span></span> <br/> |<span data-ttu-id="130d4-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="130d4-134">Optional</span></span>  <br/> |<span data-ttu-id="130d4-135">**Número**</span><span class="sxs-lookup"><span data-stu-id="130d4-135">**Number**</span></span> <br/> |<span data-ttu-id="130d4-136">El calendario usado para dar formato a las imágenes de fecha y hora de Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="130d4-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="130d4-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="130d4-137">Return value</span></span>

<span data-ttu-id="130d4-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="130d4-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="130d4-139">Notas</span><span class="sxs-lookup"><span data-stu-id="130d4-139">Remarks</span></span>

<span data-ttu-id="130d4-140">El tipo de la expresión y el tipo especificado en el formato de imagen controlan el comportamiento de la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="130d4-140">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="130d4-141">El formato debe ser adecuado para el tipo de expresión.</span><span class="sxs-lookup"><span data-stu-id="130d4-141">The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="130d4-142">El argumento unidadesDeOrigen se usa para escalar los resultados de expresiones sin tipo, por ejemplo 3 + 4.</span><span class="sxs-lookup"><span data-stu-id="130d4-142">The srcUnit argument is used to scale untyped expression results, such as 3 + 4.</span></span> <span data-ttu-id="130d4-143">Si el resultado de expresión tiene un tipo explícito, como 3 ft + 8 ft, a continuación, unidadesDeOrigen se omite.</span><span class="sxs-lookup"><span data-stu-id="130d4-143">If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="130d4-144">El argumento unidadesDeDestino se utiliza para especificar las unidades utilizadas para el resultado con formato.</span><span class="sxs-lookup"><span data-stu-id="130d4-144">The dstUnit argument is used to specify the units used for the formatted result.</span></span> <span data-ttu-id="130d4-145">Si no se especifica las unidadesDeDestino, se utilizan las unidades para el resultado de la expresión.</span><span class="sxs-lookup"><span data-stu-id="130d4-145">If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="130d4-146">Devuelve un error si el resultado de la expresión y el tipo esperado en formato son de un tipo diferente, si hay errores de sintaxis en formato o si no reconoce las unidades que se pasa como unidadesDeOrigen o unidadesDeDestino.</span><span class="sxs-lookup"><span data-stu-id="130d4-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="130d4-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="130d4-147">Example</span></span>

<span data-ttu-id="130d4-148">FORMATEX(5,5; "0,00 u", "cm", "ft")</span><span class="sxs-lookup"><span data-stu-id="130d4-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="130d4-149">Devuelve 0,18 pies.</span><span class="sxs-lookup"><span data-stu-id="130d4-149">Returns 0.18 feet.</span></span> 
  

