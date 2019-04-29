---
title: Función SECOND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Devuelve un valor integer, de 0 a 59, que representa el componente de segundos de fecha y hora o de expresión.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404879"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="1915b-103">Función SECOND (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="1915b-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="1915b-104">Devuelve un valor integer, de 0 a 59, que representa el componente de segundos de _fecha y hora_ o de _expresión_.</span><span class="sxs-lookup"><span data-stu-id="1915b-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1915b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1915b-105">Syntax</span></span>

<span data-ttu-id="1915b-106">SEGUNDO ("\* \* *DateTime* \* \*" | \* \* *expresión* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="1915b-106">SECOND(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1915b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1915b-107">Parameters</span></span>

|<span data-ttu-id="1915b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1915b-108">**Name**</span></span>|<span data-ttu-id="1915b-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="1915b-109">**Required/Optional**</span></span>|<span data-ttu-id="1915b-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="1915b-110">**Data Type**</span></span>|<span data-ttu-id="1915b-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1915b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1915b-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="1915b-112">_datetime_</span></span> <br/> |<span data-ttu-id="1915b-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1915b-113">Required</span></span>  <br/> |<span data-ttu-id="1915b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1915b-114">**String**</span></span> <br/> |<span data-ttu-id="1915b-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="1915b-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="1915b-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="1915b-116">_expression_</span></span> <br/> |<span data-ttu-id="1915b-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1915b-117">Required</span></span>  <br/> |<span data-ttu-id="1915b-118">**String**</span><span class="sxs-lookup"><span data-stu-id="1915b-118">**String**</span></span> <br/> | <span data-ttu-id="1915b-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="1915b-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="1915b-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="1915b-120">_lcid_</span></span> <br/> |<span data-ttu-id="1915b-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="1915b-121">Optional</span></span>  <br/> |<span data-ttu-id="1915b-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="1915b-122">**Numeric**</span></span> <br/> |<span data-ttu-id="1915b-123">El identificador de configuración regional que se va a usar para evaluar un _valor DateTime_que no sea local.</span><span class="sxs-lookup"><span data-stu-id="1915b-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="1915b-124">El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="1915b-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1915b-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1915b-125">Return value</span></span>

<span data-ttu-id="1915b-126">Entero</span><span class="sxs-lookup"><span data-stu-id="1915b-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1915b-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1915b-127">Remarks</span></span>

<span data-ttu-id="1915b-128">Se descarta el componente de fecha de fecha _y hora_ o de _expresión_ .</span><span class="sxs-lookup"><span data-stu-id="1915b-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="1915b-129">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="1915b-129">No rounding is done.</span></span> <span data-ttu-id="1915b-130">Si falta _fecha y hora_ o no se puede convertir en un resultado válido, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="1915b-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="1915b-131">La segunda función también acepta un único valor numérico en _expresión_ , en el que la parte decimal del resultado representa la fracción de un día contada a partir de la medianoche.</span><span class="sxs-lookup"><span data-stu-id="1915b-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="1915b-132">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="1915b-132">Example 1</span></span>

<span data-ttu-id="1915b-133">SEGUNDO ("05/30/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="1915b-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="1915b-134">Devuelve 32.</span><span class="sxs-lookup"><span data-stu-id="1915b-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1915b-135">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="1915b-135">Example 2</span></span>

<span data-ttu-id="1915b-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span><span class="sxs-lookup"><span data-stu-id="1915b-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="1915b-137">Devuelve 52.</span><span class="sxs-lookup"><span data-stu-id="1915b-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="1915b-138">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="1915b-138">Example 3</span></span>

<span data-ttu-id="1915b-139">SEGUNDO (0.6337)</span><span class="sxs-lookup"><span data-stu-id="1915b-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="1915b-140">Devuelve 32.</span><span class="sxs-lookup"><span data-stu-id="1915b-140">Returns 32.</span></span>
  

