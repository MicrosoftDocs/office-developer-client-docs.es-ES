---
title: Función WEEKDAY (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Devuelve un número entero, de 1 a 7, que representa el día de la semana en fecha y hora o expresión.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404809"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="2df8f-103">Función WEEKDAY (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="2df8f-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="2df8f-104">Devuelve un número entero, de 1 a 7, que representa el día de la semana  _en fecha y hora_ o  _expresión_.</span><span class="sxs-lookup"><span data-stu-id="2df8f-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2df8f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2df8f-105">Syntax</span></span>

<span data-ttu-id="2df8f-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="2df8f-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2df8f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2df8f-107">Parameters</span></span>

|<span data-ttu-id="2df8f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2df8f-108">**Name**</span></span>|<span data-ttu-id="2df8f-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="2df8f-109">**Required/Optional**</span></span>|<span data-ttu-id="2df8f-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2df8f-110">**Data Type**</span></span>|<span data-ttu-id="2df8f-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2df8f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2df8f-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="2df8f-112">_datetime_</span></span> <br/> |<span data-ttu-id="2df8f-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2df8f-113">Required</span></span>  <br/> |<span data-ttu-id="2df8f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="2df8f-114">**String**</span></span> <br/> | <span data-ttu-id="2df8f-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="2df8f-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="2df8f-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="2df8f-116">_expression_</span></span> <br/> |<span data-ttu-id="2df8f-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="2df8f-117">Required</span></span>  <br/> |<span data-ttu-id="2df8f-118">**Varía**</span><span class="sxs-lookup"><span data-stu-id="2df8f-118">**Varies**</span></span> <br/> |<span data-ttu-id="2df8f-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="2df8f-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="2df8f-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="2df8f-120">_lcid_</span></span> <br/> |<span data-ttu-id="2df8f-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="2df8f-121">Optional</span></span>  <br/> |<span data-ttu-id="2df8f-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="2df8f-122">**Numeric**</span></span> <br/> |<span data-ttu-id="2df8f-123">Identificador regional que se usa para evaluar información de fecha y hora que no sea local.</span><span class="sxs-lookup"><span data-stu-id="2df8f-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="2df8f-124">El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="2df8f-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2df8f-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2df8f-125">Return value</span></span>

<span data-ttu-id="2df8f-126">Entero</span><span class="sxs-lookup"><span data-stu-id="2df8f-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2df8f-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2df8f-127">Remarks</span></span>

<span data-ttu-id="2df8f-128">Se descarta el componente de _hora en la fecha y_ hora o la expresión. </span><span class="sxs-lookup"><span data-stu-id="2df8f-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="2df8f-129">El resultado corresponde al lunes (1) al domingo (7).</span><span class="sxs-lookup"><span data-stu-id="2df8f-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="2df8f-130">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="2df8f-130">No rounding is done.</span></span> <span data-ttu-id="2df8f-131">Si  _falta fecha_ y hora o no se puede interpretar como una fecha u hora válidas, la función devuelve un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2df8f-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="2df8f-132">error.</span><span class="sxs-lookup"><span data-stu-id="2df8f-132">error.</span></span> 
  
<span data-ttu-id="2df8f-133">La función WEEKDAY también acepta un  valor numérico único para la expresión donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899.</span><span class="sxs-lookup"><span data-stu-id="2df8f-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="2df8f-134">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="2df8f-134">Example 1</span></span>

<span data-ttu-id="2df8f-135">WEEKDAY("30 Mayo, 1999")</span><span class="sxs-lookup"><span data-stu-id="2df8f-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="2df8f-136">Devuelve 7.</span><span class="sxs-lookup"><span data-stu-id="2df8f-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2df8f-137">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="2df8f-137">Example 2</span></span>

<span data-ttu-id="2df8f-138">WEEKDAY(DATEVALUE("30 May., 1999")+2 ed.)</span><span class="sxs-lookup"><span data-stu-id="2df8f-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="2df8f-139">Devuelve 2.</span><span class="sxs-lookup"><span data-stu-id="2df8f-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="2df8f-140">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="2df8f-140">Example 3</span></span>

<span data-ttu-id="2df8f-141">WEEKDAY(35880.6337)</span><span class="sxs-lookup"><span data-stu-id="2df8f-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="2df8f-142">Devuelve 4.</span><span class="sxs-lookup"><span data-stu-id="2df8f-142">Returns 4.</span></span>
  

