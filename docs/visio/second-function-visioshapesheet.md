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
description: Devuelve un entero, de 0 a 59, que representa el componente de segundos de fecha y hora o expresión.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404879"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="3d985-103">Función SECOND (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="3d985-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="3d985-104">Devuelve un entero, de 0 a 59, que representa el componente de segundos de  _fecha y hora_ o  _expresión_.</span><span class="sxs-lookup"><span data-stu-id="3d985-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3d985-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d985-105">Syntax</span></span>

<span data-ttu-id="3d985-106">SECOND(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="3d985-106">SECOND(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3d985-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d985-107">Parameters</span></span>

|<span data-ttu-id="3d985-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3d985-108">**Name**</span></span>|<span data-ttu-id="3d985-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="3d985-109">**Required/Optional**</span></span>|<span data-ttu-id="3d985-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="3d985-110">**Data Type**</span></span>|<span data-ttu-id="3d985-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3d985-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3d985-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="3d985-112">_datetime_</span></span> <br/> |<span data-ttu-id="3d985-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3d985-113">Required</span></span>  <br/> |<span data-ttu-id="3d985-114">**String**</span><span class="sxs-lookup"><span data-stu-id="3d985-114">**String**</span></span> <br/> |<span data-ttu-id="3d985-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="3d985-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="3d985-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="3d985-116">_expression_</span></span> <br/> |<span data-ttu-id="3d985-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3d985-117">Required</span></span>  <br/> |<span data-ttu-id="3d985-118">**String**</span><span class="sxs-lookup"><span data-stu-id="3d985-118">**String**</span></span> <br/> | <span data-ttu-id="3d985-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="3d985-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="3d985-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="3d985-120">_lcid_</span></span> <br/> |<span data-ttu-id="3d985-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="3d985-121">Optional</span></span>  <br/> |<span data-ttu-id="3d985-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="3d985-122">**Numeric**</span></span> <br/> |<span data-ttu-id="3d985-123">Identificador de configuración regional que se usará para evaluar una fecha y hora no _local._</span><span class="sxs-lookup"><span data-stu-id="3d985-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="3d985-124">El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="3d985-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3d985-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d985-125">Return value</span></span>

<span data-ttu-id="3d985-126">Entero</span><span class="sxs-lookup"><span data-stu-id="3d985-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3d985-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d985-127">Remarks</span></span>

<span data-ttu-id="3d985-128">Se descarta el componente de  _fecha y_ hora  _o_ expresión.</span><span class="sxs-lookup"><span data-stu-id="3d985-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="3d985-129">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="3d985-129">No rounding is done.</span></span> <span data-ttu-id="3d985-130">Si  _falta fecha_ y hora o no se puede convertir en un resultado válido, esta función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="3d985-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="3d985-131">La función SECOND también acepta un  valor numérico único para la expresión donde la parte decimal del resultado representa la fracción de un día desde la medianoche.</span><span class="sxs-lookup"><span data-stu-id="3d985-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="3d985-132">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d985-132">Example 1</span></span>

<span data-ttu-id="3d985-133">SECOND("30/05/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="3d985-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="3d985-134">Devuelve 32.</span><span class="sxs-lookup"><span data-stu-id="3d985-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3d985-135">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="3d985-135">Example 2</span></span>

<span data-ttu-id="3d985-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span><span class="sxs-lookup"><span data-stu-id="3d985-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="3d985-137">Devuelve 52.</span><span class="sxs-lookup"><span data-stu-id="3d985-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="3d985-138">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="3d985-138">Example 3</span></span>

<span data-ttu-id="3d985-139">SECOND(0.6337)</span><span class="sxs-lookup"><span data-stu-id="3d985-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="3d985-140">Devuelve 32.</span><span class="sxs-lookup"><span data-stu-id="3d985-140">Returns 32.</span></span>
  

