---
title: SECOND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Devuelve un entero entre 0 y 59, que representa el componente de segundos de fecha y hora o expresión.
ms.openlocfilehash: 5f0a3e87763bd4ea5436afe221e12477e9186356
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823108"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="d1426-103">SECOND Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d1426-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d1426-104">Devuelve un entero entre 0 y 59, que representa el componente de segundos de _fecha y hora_ o _expresión_.</span><span class="sxs-lookup"><span data-stu-id="d1426-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d1426-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1426-105">Syntax</span></span>

<span data-ttu-id="d1426-106">SEGUNDO ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="d1426-106">SECOND(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d1426-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1426-107">Parameters</span></span>

|<span data-ttu-id="d1426-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d1426-108">**Name**</span></span>|<span data-ttu-id="d1426-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="d1426-109">**Required/Optional**</span></span>|<span data-ttu-id="d1426-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="d1426-110">**Data Type**</span></span>|<span data-ttu-id="d1426-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d1426-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d1426-112">_fecha y hora_</span><span class="sxs-lookup"><span data-stu-id="d1426-112">_datetime_</span></span> <br/> |<span data-ttu-id="d1426-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d1426-113">Required</span></span>  <br/> |<span data-ttu-id="d1426-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d1426-114">**String**</span></span> <br/> |<span data-ttu-id="d1426-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="d1426-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="d1426-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="d1426-116">_expression_</span></span> <br/> |<span data-ttu-id="d1426-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d1426-117">Required</span></span>  <br/> |<span data-ttu-id="d1426-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d1426-118">**String**</span></span> <br/> | <span data-ttu-id="d1426-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="d1426-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="d1426-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="d1426-120">_lcid_</span></span> <br/> |<span data-ttu-id="d1426-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="d1426-121">Optional</span></span>  <br/> |<span data-ttu-id="d1426-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="d1426-122">**Numeric**</span></span> <br/> |<span data-ttu-id="d1426-123">El identificador de configuración regional que se utiliza para evaluar una _fecha y hora_de no locales.</span><span class="sxs-lookup"><span data-stu-id="d1426-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="d1426-124">El identificador de configuración regional es un número que se describen en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="d1426-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d1426-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1426-125">Return value</span></span>

<span data-ttu-id="d1426-126">Entero</span><span class="sxs-lookup"><span data-stu-id="d1426-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1426-127">Notas</span><span class="sxs-lookup"><span data-stu-id="d1426-127">Remarks</span></span>

<span data-ttu-id="d1426-128">La fecha _y hora_ o de _expresión_ se descarta.</span><span class="sxs-lookup"><span data-stu-id="d1426-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="d1426-129">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="d1426-129">No rounding is done.</span></span> <span data-ttu-id="d1426-130">Si falta _fecha y hora_ o si no se puede convertir en un resultado válido, esta función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="d1426-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="d1426-131">La función SECOND también acepta un único valor numérico en _expresión_ , donde la parte decimal del resultado representa la fracción de un día contada a partir de la medianoche.</span><span class="sxs-lookup"><span data-stu-id="d1426-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d1426-132">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="d1426-132">Example 1</span></span>

<span data-ttu-id="d1426-133">SECOND("05/30/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="d1426-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="d1426-134">Devuelve 32.</span><span class="sxs-lookup"><span data-stu-id="d1426-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d1426-135">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="d1426-135">Example 2</span></span>

<span data-ttu-id="d1426-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span><span class="sxs-lookup"><span data-stu-id="d1426-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="d1426-137">Devuelve 52.</span><span class="sxs-lookup"><span data-stu-id="d1426-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d1426-138">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="d1426-138">Example 3</span></span>

<span data-ttu-id="d1426-139">SECOND(0.6337)</span><span class="sxs-lookup"><span data-stu-id="d1426-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="d1426-140">Devuelve 32.</span><span class="sxs-lookup"><span data-stu-id="d1426-140">Returns 32.</span></span>
  

