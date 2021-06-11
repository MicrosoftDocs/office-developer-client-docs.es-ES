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
description: Devuelve un número entero, de 0 a 23, que representa la hora del día de fecha y hora o expresión.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429638"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="1333f-103">Función HOUR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="1333f-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="1333f-104">Devuelve un entero, de 0 a 23, que representa la hora del día de  _datetime_ o  _expresión_.</span><span class="sxs-lookup"><span data-stu-id="1333f-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1333f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1333f-105">Syntax</span></span>

<span data-ttu-id="1333f-106">HOUR(" \*\* *datetime* \*\* "| \*\* *expresión* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="1333f-106">HOUR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1333f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1333f-107">Parameters</span></span>

|<span data-ttu-id="1333f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1333f-108">**Name**</span></span>|<span data-ttu-id="1333f-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="1333f-109">**Required/Optional**</span></span>|<span data-ttu-id="1333f-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="1333f-110">**Data Type**</span></span>|<span data-ttu-id="1333f-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1333f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1333f-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="1333f-112">_datetime_</span></span> <br/> |<span data-ttu-id="1333f-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1333f-113">Required</span></span>  <br/> |<span data-ttu-id="1333f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1333f-114">**String**</span></span> <br/> | <span data-ttu-id="1333f-115">Una cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="1333f-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="1333f-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="1333f-116">_expression_</span></span> <br/> |<span data-ttu-id="1333f-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1333f-117">Required</span></span>  <br/> |<span data-ttu-id="1333f-118">**Varía**</span><span class="sxs-lookup"><span data-stu-id="1333f-118">**Varies**</span></span> <br/> |<span data-ttu-id="1333f-119">Una expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="1333f-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="1333f-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="1333f-120">_lcid_</span></span> <br/> |<span data-ttu-id="1333f-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="1333f-121">Optional</span></span>  <br/> |<span data-ttu-id="1333f-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="1333f-122">**Number**</span></span> <br/> | <span data-ttu-id="1333f-p101">Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="1333f-p101">A locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1333f-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1333f-125">Remarks</span></span>

<span data-ttu-id="1333f-126">El componente date en  *datetime*  y  *expresión*  se descarta.</span><span class="sxs-lookup"><span data-stu-id="1333f-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="1333f-127">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="1333f-127">No rounding is done.</span></span> <span data-ttu-id="1333f-128">Si falta  *la fecha y hora*  o no se puede convertir en un resultado válido, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="1333f-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="1333f-129">El formato del valor devuelto corresponde al estilo de hora establecido en la configuración regional actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="1333f-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="1333f-130">La función HOUR también acepta un  valor numérico único para la expresión donde la parte decimal del resultado representa la fracción de un día desde la medianoche.</span><span class="sxs-lookup"><span data-stu-id="1333f-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="1333f-131">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="1333f-131">Example 1</span></span>

<span data-ttu-id="1333f-132">HOUR("15:45")</span><span class="sxs-lookup"><span data-stu-id="1333f-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="1333f-133">Devuelve 15.</span><span class="sxs-lookup"><span data-stu-id="1333f-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1333f-134">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="1333f-134">Example 2</span></span>

<span data-ttu-id="1333f-135">HOUR("Mayo 30, 1997 3:45:24 pm")</span><span class="sxs-lookup"><span data-stu-id="1333f-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="1333f-136">Devuelve 15.</span><span class="sxs-lookup"><span data-stu-id="1333f-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="1333f-137">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="1333f-137">Example 3</span></span>

<span data-ttu-id="1333f-138">HOUR(0.5)</span><span class="sxs-lookup"><span data-stu-id="1333f-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="1333f-139">Devuelve 12.</span><span class="sxs-lookup"><span data-stu-id="1333f-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="1333f-140">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="1333f-140">Example 4</span></span>

<span data-ttu-id="1333f-141">HOUR("5/30/1997")</span><span class="sxs-lookup"><span data-stu-id="1333f-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="1333f-142">Devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="1333f-142">Returns 0.</span></span>
  

