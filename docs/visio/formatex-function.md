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
description: Devuelve el resultado de la expresión evaluada en srcUnit como una cadena con formato de acuerdo con el formato expresado en dstUnit.
ms.openlocfilehash: e341cbcb16cc273f0413f98c195f77ad08946ab1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430969"
---
# <a name="formatex-function"></a><span data-ttu-id="614b1-103">Función FORMATEX</span><span class="sxs-lookup"><span data-stu-id="614b1-103">FORMATEX Function</span></span>

<span data-ttu-id="614b1-104">Devuelve el resultado de la expresión evaluada en srcUnit como una cadena con formato de acuerdo con el formato expresado en dstUnit.</span><span class="sxs-lookup"><span data-stu-id="614b1-104">Returns the result of expression evaluated in srcUnit as a string formatted according to format expressed in dstUnit.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="614b1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="614b1-105">Syntax</span></span>

<span data-ttu-id="614b1-106">FORMATEX(\*\* *expresión* \*\*," \*\* *format* \*\* ",[ \*\* *srcUnit* \*\* ],[ \*\* *dstUnit* \*\* ],[ \*\* *langID* \*\* ][, \*\* *calID* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="614b1-106">FORMATEX(\*\* *expression* \*\*," \*\* *format* \*\* ",[ \*\* *srcUnit* \*\* ],[ \*\* *dstUnit* \*\* ],[ \*\* *langID* \*\* ][, \*\* *calID* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="614b1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="614b1-107">Parameters</span></span>

|<span data-ttu-id="614b1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="614b1-108">**Name**</span></span>|<span data-ttu-id="614b1-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="614b1-109">**Required/Optional**</span></span>|<span data-ttu-id="614b1-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="614b1-110">**Data Type**</span></span>|<span data-ttu-id="614b1-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="614b1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="614b1-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="614b1-112">_expression_</span></span> <br/> |<span data-ttu-id="614b1-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="614b1-113">Required</span></span>  <br/> |<span data-ttu-id="614b1-114">**String**</span><span class="sxs-lookup"><span data-stu-id="614b1-114">**String**</span></span> <br/> |<span data-ttu-id="614b1-115">Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor.</span><span class="sxs-lookup"><span data-stu-id="614b1-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="614b1-116">_format_</span><span class="sxs-lookup"><span data-stu-id="614b1-116">_format_</span></span> <br/> |<span data-ttu-id="614b1-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="614b1-117">Required</span></span>  <br/> |<span data-ttu-id="614b1-118">**String**</span><span class="sxs-lookup"><span data-stu-id="614b1-118">**String**</span></span> <br/> |<span data-ttu-id="614b1-119">Imagen de formato usada para dar formato a la cadena.</span><span class="sxs-lookup"><span data-stu-id="614b1-119">The format picture used to format the string.</span></span> <span data-ttu-id="614b1-120">Para obtener más información acerca del formato de imágenes, vea [Acerca del formato de imágenes](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="614b1-120">For more information about format pictures, see [About Format Pictures](about-format-pictures.md).</span></span>  <br/> |
| <span data-ttu-id="614b1-121">_srcUnit_</span><span class="sxs-lookup"><span data-stu-id="614b1-121">_srcUnit_</span></span> <br/> |<span data-ttu-id="614b1-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="614b1-122">Optional</span></span>  <br/> |<span data-ttu-id="614b1-123">**String**</span><span class="sxs-lookup"><span data-stu-id="614b1-123">**String**</span></span> <br/> | <span data-ttu-id="614b1-124">Unidades usadas para evaluar expresión (pda, cm, etc.).</span><span class="sxs-lookup"><span data-stu-id="614b1-124">Units used to evaluate expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="614b1-125">_dstUnit_</span><span class="sxs-lookup"><span data-stu-id="614b1-125">_dstUnit_</span></span> <br/> |<span data-ttu-id="614b1-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="614b1-126">Optional</span></span>  <br/> |<span data-ttu-id="614b1-127">**String**</span><span class="sxs-lookup"><span data-stu-id="614b1-127">**String**</span></span> <br/> |<span data-ttu-id="614b1-128">Unidades usadas para el resultado de expresión (pda, cm, etc.).</span><span class="sxs-lookup"><span data-stu-id="614b1-128">Units to use for the result of expression (in, cm, and so forth).</span></span>  <br/> |
| <span data-ttu-id="614b1-129">_langID_</span><span class="sxs-lookup"><span data-stu-id="614b1-129">_langID_</span></span> <br/> |<span data-ttu-id="614b1-130">Opcional</span><span class="sxs-lookup"><span data-stu-id="614b1-130">Optional</span></span>  <br/> |<span data-ttu-id="614b1-131">**Number**</span><span class="sxs-lookup"><span data-stu-id="614b1-131">**Number**</span></span> <br/> |<span data-ttu-id="614b1-132">El idioma utilizado para dar formato a las imágenes de fecha y hora de Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="614b1-132">The language used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
| <span data-ttu-id="614b1-133">_calID_</span><span class="sxs-lookup"><span data-stu-id="614b1-133">_calID_</span></span> <br/> |<span data-ttu-id="614b1-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="614b1-134">Optional</span></span>  <br/> |<span data-ttu-id="614b1-135">**Number**</span><span class="sxs-lookup"><span data-stu-id="614b1-135">**Number**</span></span> <br/> |<span data-ttu-id="614b1-136">El calendario usado para dar formato a las imágenes de fecha y hora de Microsoft Office System.</span><span class="sxs-lookup"><span data-stu-id="614b1-136">The calendar used when formatting Microsoft Office System date/time pictures.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="614b1-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="614b1-137">Return value</span></span>

<span data-ttu-id="614b1-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="614b1-138">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="614b1-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="614b1-139">Remarks</span></span>

<span data-ttu-id="614b1-p102">El tipo de la expresión y el especificado en el formato de imagen controlan el comportamiento de la cadena devuelta. El valor de formato debe ser adecuado para el tipo de expresión.</span><span class="sxs-lookup"><span data-stu-id="614b1-p102">The type of the expression and the type specified in the format picture govern the behavior of the returned string. The format must be appropriate for the type of expression.</span></span>
  
<span data-ttu-id="614b1-p103">El argumento unidadesDeOrigen se utiliza para dar la escala adecuada a los resultados de la expresión que carecen de tipo, por ejemplo 3 + 4. Si el resultado de expresión tiene un tipo explícito, como 3 m + 8 m, no se tiene en cuenta el valor de unidadesDeOrigen.</span><span class="sxs-lookup"><span data-stu-id="614b1-p103">The srcUnit argument is used to scale untyped expression results, such as 3 + 4. If the result of expression has an explicit type, such as 3 ft + 8 ft, then srcUnit is ignored.</span></span>
  
<span data-ttu-id="614b1-p104">El argumento unidadesDeDestino se utiliza para especificar las unidades que se usan en el resultado con formato. Si no se especifican las unidadesDeDestino, se utilizan las unidades del resultado de la expresión.</span><span class="sxs-lookup"><span data-stu-id="614b1-p104">The dstUnit argument is used to specify the units used for the formatted result. If dstUnit is not specified, the units for the result of the expression are used.</span></span>
  
<span data-ttu-id="614b1-146">Devuelve un error si el resultado de la expresión y el tipo esperado en formato son distintos, si hay errores de sintaxis en formato o si no se reconocen las unidades especificadas como unidadesDeOrigen o unidadesDeDestino.</span><span class="sxs-lookup"><span data-stu-id="614b1-146">Returns an error if the result of expression and the type expected in format are of a different kind, if there are syntax errors in format, or if it does not recognize the units passed as srcUnit or dstUnit.</span></span>
  
## <a name="example"></a><span data-ttu-id="614b1-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="614b1-147">Example</span></span>

<span data-ttu-id="614b1-148">FORMATEX(5,5; "0,00 u", "cm", "ft")</span><span class="sxs-lookup"><span data-stu-id="614b1-148">FORMATEX(5.5, "0.00 u", "cm", "ft")</span></span> 
  
<span data-ttu-id="614b1-149">Devuelve 0,18 pies.</span><span class="sxs-lookup"><span data-stu-id="614b1-149">Returns 0.18 feet.</span></span> 
  

