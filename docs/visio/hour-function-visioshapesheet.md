---
title: HOUR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Devuelve un entero entre 0 y 23, que representa la hora del día de fecha y hora o expresión.
ms.openlocfilehash: 9cfe8c88a4a4d73be23b2ac230b0cfabc955c004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822293"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="88ffd-103">HOUR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="88ffd-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="88ffd-104">Devuelve un entero entre 0 y 23, que representa la hora del día de _fecha y hora_ o _expresión_.</span><span class="sxs-lookup"><span data-stu-id="88ffd-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="88ffd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88ffd-105">Syntax</span></span>

<span data-ttu-id="88ffd-106">HORA ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="88ffd-106">HOUR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="88ffd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88ffd-107">Parameters</span></span>

|<span data-ttu-id="88ffd-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="88ffd-108">**Name**</span></span>|<span data-ttu-id="88ffd-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="88ffd-109">**Required/Optional**</span></span>|<span data-ttu-id="88ffd-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="88ffd-110">**Data Type**</span></span>|<span data-ttu-id="88ffd-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88ffd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="88ffd-112">_fecha y hora_</span><span class="sxs-lookup"><span data-stu-id="88ffd-112">_datetime_</span></span> <br/> |<span data-ttu-id="88ffd-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="88ffd-113">Required</span></span>  <br/> |<span data-ttu-id="88ffd-114">**String**</span><span class="sxs-lookup"><span data-stu-id="88ffd-114">**String**</span></span> <br/> | <span data-ttu-id="88ffd-115">Una cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="88ffd-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="88ffd-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="88ffd-116">_expression_</span></span> <br/> |<span data-ttu-id="88ffd-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="88ffd-117">Required</span></span>  <br/> |<span data-ttu-id="88ffd-118">**Varies**</span><span class="sxs-lookup"><span data-stu-id="88ffd-118">**Varies**</span></span> <br/> |<span data-ttu-id="88ffd-119">Una expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="88ffd-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="88ffd-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="88ffd-120">_lcid_</span></span> <br/> |<span data-ttu-id="88ffd-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="88ffd-121">Optional</span></span>  <br/> |<span data-ttu-id="88ffd-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="88ffd-122">**Number**</span></span> <br/> | <span data-ttu-id="88ffd-p101">Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="88ffd-p101">A locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88ffd-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88ffd-125">Remarks</span></span>

<span data-ttu-id="88ffd-126">La fecha y *hora* o de *expresión* se descarta.</span><span class="sxs-lookup"><span data-stu-id="88ffd-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="88ffd-127">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="88ffd-127">No rounding is done.</span></span> <span data-ttu-id="88ffd-128">Si la *fecha y hora* falta o no se puede convertir en un resultado válido, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="88ffd-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="88ffd-129">El formato del valor devuelto corresponde al estilo de hora establecido en la configuración regional actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="88ffd-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="88ffd-130">La función HOUR también acepta un único valor numérico en *expresión* , donde la parte decimal del resultado representa la fracción de un día contada a partir de la medianoche.</span><span class="sxs-lookup"><span data-stu-id="88ffd-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="88ffd-131">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="88ffd-131">Example 1</span></span>

<span data-ttu-id="88ffd-132">HOUR("15:45")</span><span class="sxs-lookup"><span data-stu-id="88ffd-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="88ffd-133">Devuelve 15.</span><span class="sxs-lookup"><span data-stu-id="88ffd-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="88ffd-134">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="88ffd-134">Example 2</span></span>

<span data-ttu-id="88ffd-135">HOUR("Mayo 30, 1997 3:45:24 pm")</span><span class="sxs-lookup"><span data-stu-id="88ffd-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="88ffd-136">Devuelve 15.</span><span class="sxs-lookup"><span data-stu-id="88ffd-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="88ffd-137">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="88ffd-137">Example 3</span></span>

<span data-ttu-id="88ffd-138">HOUR(0.5)</span><span class="sxs-lookup"><span data-stu-id="88ffd-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="88ffd-139">Devuelve 12.</span><span class="sxs-lookup"><span data-stu-id="88ffd-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="88ffd-140">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="88ffd-140">Example 4</span></span>

<span data-ttu-id="88ffd-141">HOUR("5/30/1997")</span><span class="sxs-lookup"><span data-stu-id="88ffd-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="88ffd-142">Devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="88ffd-142">Returns 0.</span></span>
  

