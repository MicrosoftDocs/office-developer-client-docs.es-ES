---
title: Función HOUR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Devuelve un valor integer, entre 0 y 23, que representa la hora del día de la fecha y hora o de una expresión.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429638"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="d0986-103">Función HOUR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d0986-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d0986-104">Devuelve un valor integer, entre 0 y 23, que representa la hora del día de la _fecha y hora_ o de una _expresión_.</span><span class="sxs-lookup"><span data-stu-id="d0986-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d0986-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0986-105">Syntax</span></span>

<span data-ttu-id="d0986-106">HOUR ("\* \* *DateTime* \* \*" | \* \* *expresión* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="d0986-106">HOUR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d0986-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0986-107">Parameters</span></span>

|<span data-ttu-id="d0986-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d0986-108">**Name**</span></span>|<span data-ttu-id="d0986-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="d0986-109">**Required/Optional**</span></span>|<span data-ttu-id="d0986-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="d0986-110">**Data Type**</span></span>|<span data-ttu-id="d0986-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0986-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d0986-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="d0986-112">_datetime_</span></span> <br/> |<span data-ttu-id="d0986-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d0986-113">Required</span></span>  <br/> |<span data-ttu-id="d0986-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d0986-114">**String**</span></span> <br/> | <span data-ttu-id="d0986-115">Una cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="d0986-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="d0986-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="d0986-116">_expression_</span></span> <br/> |<span data-ttu-id="d0986-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d0986-117">Required</span></span>  <br/> |<span data-ttu-id="d0986-118">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="d0986-118">**Varies**</span></span> <br/> |<span data-ttu-id="d0986-119">Una expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="d0986-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="d0986-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="d0986-120">_lcid_</span></span> <br/> |<span data-ttu-id="d0986-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="d0986-121">Optional</span></span>  <br/> |<span data-ttu-id="d0986-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="d0986-122">**Number**</span></span> <br/> | <span data-ttu-id="d0986-123">Identificador regional que se usa para evaluar información de fecha y hora que no sea local.</span><span class="sxs-lookup"><span data-stu-id="d0986-123">A locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="d0986-124">El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="d0986-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0986-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0986-125">Remarks</span></span>

<span data-ttu-id="d0986-126">Se descarta el componente de fecha de *DateTime* y de *expresión* .</span><span class="sxs-lookup"><span data-stu-id="d0986-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="d0986-127">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="d0986-127">No rounding is done.</span></span> <span data-ttu-id="d0986-128">Si falta el *valor de fecha y hora* o no se puede convertir en un resultado válido, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="d0986-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="d0986-129">El formato del valor devuelto corresponde al estilo de hora establecido en la configuración regional actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="d0986-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="d0986-130">La función HOUR también acepta un único valor numérico en *expresión* , en el que la parte decimal del resultado representa la fracción de un día contada a partir de la medianoche.</span><span class="sxs-lookup"><span data-stu-id="d0986-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d0986-131">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0986-131">Example 1</span></span>

<span data-ttu-id="d0986-132">HOUR ("15:45")</span><span class="sxs-lookup"><span data-stu-id="d0986-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="d0986-133">Devuelve 15.</span><span class="sxs-lookup"><span data-stu-id="d0986-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d0986-134">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="d0986-134">Example 2</span></span>

<span data-ttu-id="d0986-135">HOUR("Mayo 30, 1997 3:45:24 pm")</span><span class="sxs-lookup"><span data-stu-id="d0986-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="d0986-136">Devuelve 15.</span><span class="sxs-lookup"><span data-stu-id="d0986-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d0986-137">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="d0986-137">Example 3</span></span>

<span data-ttu-id="d0986-138">HORA (0,5)</span><span class="sxs-lookup"><span data-stu-id="d0986-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="d0986-139">Devuelve 12.</span><span class="sxs-lookup"><span data-stu-id="d0986-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="d0986-140">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="d0986-140">Example 4</span></span>

<span data-ttu-id="d0986-141">HOUR ("5/30/1997")</span><span class="sxs-lookup"><span data-stu-id="d0986-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="d0986-142">Devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="d0986-142">Returns 0.</span></span>
  

