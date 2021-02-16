---
title: Función MINUTE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Devuelve un entero de 0 a 59 que representa el componente de minutos de fecha y hora o expresión .
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436569"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="51e53-103">Función MINUTE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="51e53-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="51e53-104">Devuelve un entero entre 0 y 59 que representa el componente de minutos de  *fecha y hora*  o  *expresión*  .</span><span class="sxs-lookup"><span data-stu-id="51e53-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="51e53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51e53-105">Syntax</span></span>

<span data-ttu-id="51e53-106">MINUTE(" *datetime*  "|  *expresión*  [,  *lcid*  ])</span><span class="sxs-lookup"><span data-stu-id="51e53-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="51e53-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51e53-107">Parameters</span></span>

|<span data-ttu-id="51e53-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="51e53-108">**Name**</span></span>|<span data-ttu-id="51e53-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="51e53-109">**Required/Optional**</span></span>|<span data-ttu-id="51e53-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="51e53-110">**Data Type**</span></span>|<span data-ttu-id="51e53-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="51e53-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="51e53-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="51e53-112">_datetime_</span></span> <br/> |<span data-ttu-id="51e53-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="51e53-113">Required</span></span>  <br/> |<span data-ttu-id="51e53-114">**String**</span><span class="sxs-lookup"><span data-stu-id="51e53-114">**String**</span></span> <br/> |<span data-ttu-id="51e53-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="51e53-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="51e53-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="51e53-116">_expression_</span></span> <br/> |<span data-ttu-id="51e53-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="51e53-117">Required</span></span>  <br/> |<span data-ttu-id="51e53-118">**String**</span><span class="sxs-lookup"><span data-stu-id="51e53-118">**String**</span></span> <br/> | <span data-ttu-id="51e53-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="51e53-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="51e53-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="51e53-120">_lcid_</span></span> <br/> |<span data-ttu-id="51e53-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="51e53-121">Optional</span></span>  <br/> |<span data-ttu-id="51e53-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="51e53-122">**Number**</span></span> <br/> |<span data-ttu-id="51e53-123">Identificador regional que se usa para evaluar información de fecha y hora que no sea local.</span><span class="sxs-lookup"><span data-stu-id="51e53-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="51e53-124">El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="51e53-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="51e53-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51e53-125">Return value</span></span>

<span data-ttu-id="51e53-126">Entero</span><span class="sxs-lookup"><span data-stu-id="51e53-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51e53-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51e53-127">Remarks</span></span>

<span data-ttu-id="51e53-128">Se descarta el componente de  _fecha y_ hora  _y la_ expresión.</span><span class="sxs-lookup"><span data-stu-id="51e53-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="51e53-129">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="51e53-129">No rounding is done.</span></span> <span data-ttu-id="51e53-130">Si  _falta fecha y_ hora o no se puede convertir en un resultado válido, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="51e53-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="51e53-131">El formato del valor devuelto corresponde al estilo de hora establecido en la configuración regional actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="51e53-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="51e53-132">La función MINUTE también acepta un  valor numérico único para la expresión en la que la parte decimal representa la fracción de un día desde la medianoche.</span><span class="sxs-lookup"><span data-stu-id="51e53-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="51e53-133">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="51e53-133">Example 1</span></span>

<span data-ttu-id="51e53-134">MINUTE("7/7/1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="51e53-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="51e53-135">Devuelve 45.</span><span class="sxs-lookup"><span data-stu-id="51e53-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="51e53-136">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="51e53-136">Example 2</span></span>

<span data-ttu-id="51e53-137">MINUTE(TIMEVALUE("25 Ene., 1999 12:07:45")+6 em.)</span><span class="sxs-lookup"><span data-stu-id="51e53-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="51e53-138">Devuelve 13.</span><span class="sxs-lookup"><span data-stu-id="51e53-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="51e53-139">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="51e53-139">Example 3</span></span>

<span data-ttu-id="51e53-140">MINUTE(0,575)</span><span class="sxs-lookup"><span data-stu-id="51e53-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="51e53-141">Devuelve 48.</span><span class="sxs-lookup"><span data-stu-id="51e53-141">Returns 48.</span></span>
  

