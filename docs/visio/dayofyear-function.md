---
title: DAYOFYEAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Devuelve un valor integer, de 1 a 366, que representa el día secuencial del año en fechaHora o expresión. La función DAYOFYEAR usa el calendario gregoriano.
ms.openlocfilehash: 30c0331a57282baee97e81689b6a8f362581b8f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439454"
---
# <a name="dayofyear-function"></a><span data-ttu-id="40ccb-104">Función DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="40ccb-104">DAYOFYEAR Function</span></span>

<span data-ttu-id="40ccb-105">Devuelve un valor integer, de 1 a 366, que representa el día secuencial del año en _fechaHora_ o _expresión_.</span><span class="sxs-lookup"><span data-stu-id="40ccb-105">Returns an integer, 1 to 366, that represents the sequential day of the year in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="40ccb-106">La función DAYOFYEAR usa el calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="40ccb-106">The DAYOFYEAR function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="40ccb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40ccb-107">Syntax</span></span>

<span data-ttu-id="40ccb-108">DAYOFYEAR ("\* \* *DateTime* \* \*" | \* \* *expresión* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="40ccb-108">DAYOFYEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="40ccb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40ccb-109">Parameters</span></span>

|<span data-ttu-id="40ccb-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="40ccb-110">**Name**</span></span>|<span data-ttu-id="40ccb-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="40ccb-111">**Required/Optional**</span></span>|<span data-ttu-id="40ccb-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="40ccb-112">**Data Type**</span></span>|<span data-ttu-id="40ccb-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40ccb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="40ccb-114">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="40ccb-114">_datetime_</span></span> <br/> |<span data-ttu-id="40ccb-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="40ccb-115">Required</span></span>  <br/> |<span data-ttu-id="40ccb-116">**String**</span><span class="sxs-lookup"><span data-stu-id="40ccb-116">**String**</span></span> <br/> |<span data-ttu-id="40ccb-117">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="40ccb-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="40ccb-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="40ccb-118">_expression_</span></span> <br/> |<span data-ttu-id="40ccb-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="40ccb-119">Required</span></span>  <br/> |<span data-ttu-id="40ccb-120">**String**</span><span class="sxs-lookup"><span data-stu-id="40ccb-120">**String**</span></span> <br/> |<span data-ttu-id="40ccb-121">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="40ccb-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="40ccb-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="40ccb-122">_lcid_</span></span> <br/> |<span data-ttu-id="40ccb-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="40ccb-123">Optional</span></span>  <br/> |<span data-ttu-id="40ccb-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="40ccb-124">**Number**</span></span> <br/> |<span data-ttu-id="40ccb-p103">Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="40ccb-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="40ccb-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40ccb-127">Return value</span></span>

<span data-ttu-id="40ccb-128">Entero</span><span class="sxs-lookup"><span data-stu-id="40ccb-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40ccb-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40ccb-129">Remarks</span></span>

<span data-ttu-id="40ccb-130">Se descarta cualquier parte de _fecha_ y hora o de _expresión_ que contenga el componente de tiempo.</span><span class="sxs-lookup"><span data-stu-id="40ccb-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="40ccb-131">El resultado corresponde a la fecha entre el 1 de enero y el 31 de diciembre.</span><span class="sxs-lookup"><span data-stu-id="40ccb-131">The result corresponds to January 1 to December 31.</span></span> <span data-ttu-id="40ccb-132">No se realiza ningún redondeo.</span><span class="sxs-lookup"><span data-stu-id="40ccb-132">No rounding is done.</span></span> <span data-ttu-id="40ccb-133">Si falta _fechaHora_ o no se puede interpretar como una fecha u hora válidas, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="40ccb-133">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns an error.</span></span> 
  
<span data-ttu-id="40ccb-134">La función DAYOFYEAR también acepta un único valor numérico en _expresión_ , en el que la parte entera del resultado representa el número de días transcurridos desde el 30 de diciembre de 1899.</span><span class="sxs-lookup"><span data-stu-id="40ccb-134">The DAYOFYEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="40ccb-135">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="40ccb-135">Example 1</span></span>

<span data-ttu-id="40ccb-136">DAYOFYEAR("May 30, 1997 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="40ccb-136">DAYOFYEAR("May 30, 1997 13:45:24")</span></span>
  
<span data-ttu-id="40ccb-137">Devuelve 150.</span><span class="sxs-lookup"><span data-stu-id="40ccb-137">Returns 150.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="40ccb-138">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="40ccb-138">Example 2</span></span>

<span data-ttu-id="40ccb-139">DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="40ccb-139">DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="40ccb-140">Devuelve 157.</span><span class="sxs-lookup"><span data-stu-id="40ccb-140">Returns 157.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="40ccb-141">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="40ccb-141">Example 3</span></span>

<span data-ttu-id="40ccb-142">DAYOFYEAR (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="40ccb-142">DAYOFYEAR(35580.6337)</span></span>
  
<span data-ttu-id="40ccb-143">Devuelve 150.</span><span class="sxs-lookup"><span data-stu-id="40ccb-143">Returns 150.</span></span>
  

