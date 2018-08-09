---
title: MINUTE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Devuelve un valor integer entre 0 y 59 que representa el componente de minutos de fecha y hora o expresión.
ms.openlocfilehash: 7c35ec15f2cebd95bb09924ca94f20630c862360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822659"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="ce0d5-103">MINUTE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="ce0d5-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="ce0d5-104">Devuelve un valor integer entre 0 y 59 que representa el componente de minutos de *fecha y hora* o *expresión* .</span><span class="sxs-lookup"><span data-stu-id="ce0d5-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ce0d5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce0d5-105">Syntax</span></span>

<span data-ttu-id="ce0d5-106">MINUTO (" *datetime* " |  *expresión*  [, *lcid* ])</span><span class="sxs-lookup"><span data-stu-id="ce0d5-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ce0d5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce0d5-107">Parameters</span></span>

|<span data-ttu-id="ce0d5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ce0d5-108">**Name**</span></span>|<span data-ttu-id="ce0d5-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="ce0d5-109">**Required/Optional**</span></span>|<span data-ttu-id="ce0d5-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ce0d5-110">**Data Type**</span></span>|<span data-ttu-id="ce0d5-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce0d5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ce0d5-112">_fecha y hora_</span><span class="sxs-lookup"><span data-stu-id="ce0d5-112">_datetime_</span></span> <br/> |<span data-ttu-id="ce0d5-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ce0d5-113">Required</span></span>  <br/> |<span data-ttu-id="ce0d5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ce0d5-114">**String**</span></span> <br/> |<span data-ttu-id="ce0d5-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="ce0d5-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="ce0d5-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="ce0d5-116">_expression_</span></span> <br/> |<span data-ttu-id="ce0d5-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ce0d5-117">Required</span></span>  <br/> |<span data-ttu-id="ce0d5-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ce0d5-118">**String**</span></span> <br/> | <span data-ttu-id="ce0d5-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="ce0d5-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="ce0d5-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="ce0d5-120">_lcid_</span></span> <br/> |<span data-ttu-id="ce0d5-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="ce0d5-121">Optional</span></span>  <br/> |<span data-ttu-id="ce0d5-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="ce0d5-122">**Number**</span></span> <br/> |<span data-ttu-id="ce0d5-p101">Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="ce0d5-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ce0d5-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce0d5-125">Return value</span></span>

<span data-ttu-id="ce0d5-126">Entero</span><span class="sxs-lookup"><span data-stu-id="ce0d5-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ce0d5-127">Notas</span><span class="sxs-lookup"><span data-stu-id="ce0d5-127">Remarks</span></span>

<span data-ttu-id="ce0d5-128">La fecha y _hora_ o de _expresión_ se descarta.</span><span class="sxs-lookup"><span data-stu-id="ce0d5-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="ce0d5-129">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="ce0d5-129">No rounding is done.</span></span> <span data-ttu-id="ce0d5-130">Si falta _fecha y hora_ o si no se puede convertir en un resultado válido, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="ce0d5-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="ce0d5-131">El formato del valor devuelto corresponde al estilo de hora establecido en la configuración regional actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="ce0d5-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="ce0d5-132">La función MINUTE también acepta un único valor numérico en _expresión_ , donde la parte decimal representa la fracción de un día contada a partir de la medianoche.</span><span class="sxs-lookup"><span data-stu-id="ce0d5-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ce0d5-133">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce0d5-133">Example 1</span></span>

<span data-ttu-id="ce0d5-134">MINUTE("7/7/1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="ce0d5-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="ce0d5-135">Devuelve 45.</span><span class="sxs-lookup"><span data-stu-id="ce0d5-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ce0d5-136">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce0d5-136">Example 2</span></span>

<span data-ttu-id="ce0d5-137">MINUTE(TIMEVALUE("25 Ene., 1999 12:07:45")+6 em.)</span><span class="sxs-lookup"><span data-stu-id="ce0d5-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="ce0d5-138">Devuelve 13.</span><span class="sxs-lookup"><span data-stu-id="ce0d5-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ce0d5-139">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="ce0d5-139">Example 3</span></span>

<span data-ttu-id="ce0d5-140">MINUTE(0.575)</span><span class="sxs-lookup"><span data-stu-id="ce0d5-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="ce0d5-141">Devuelve 48.</span><span class="sxs-lookup"><span data-stu-id="ce0d5-141">Returns 48.</span></span>
  

