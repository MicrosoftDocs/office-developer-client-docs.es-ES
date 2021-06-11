---
title: Función TIMEVALUE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Devuelve el valor de hora representado por fecha y hora o expresión, en función de la configuración de región e idioma del sistema.
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432327"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="6a501-103">Función TIMEVALUE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="6a501-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="6a501-104">Devuelve el valor de hora representado por  _datetime_ o  _expresión_, en función de la configuración de región e idioma del sistema.</span><span class="sxs-lookup"><span data-stu-id="6a501-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6a501-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a501-105">Syntax</span></span>

<span data-ttu-id="6a501-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expresión* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="6a501-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6a501-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a501-107">Parameters</span></span>

|<span data-ttu-id="6a501-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6a501-108">**Name**</span></span>|<span data-ttu-id="6a501-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="6a501-109">**Required/Optional**</span></span>|<span data-ttu-id="6a501-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="6a501-110">**Data Type**</span></span>|<span data-ttu-id="6a501-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a501-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6a501-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="6a501-112">_datetime_</span></span> <br/> |<span data-ttu-id="6a501-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6a501-113">Required</span></span>  <br/> |<span data-ttu-id="6a501-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6a501-114">**String**</span></span> <br/> | <span data-ttu-id="6a501-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="6a501-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="6a501-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="6a501-116">_expression_</span></span> <br/> |<span data-ttu-id="6a501-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6a501-117">Required</span></span>  <br/> |<span data-ttu-id="6a501-118">**Varía**</span><span class="sxs-lookup"><span data-stu-id="6a501-118">**Varies**</span></span> <br/> | <span data-ttu-id="6a501-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="6a501-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="6a501-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="6a501-120">_lcid_</span></span> <br/> |<span data-ttu-id="6a501-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="6a501-121">Optional</span></span>  <br/> |<span data-ttu-id="6a501-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="6a501-122">**Number**</span></span> <br/> |<span data-ttu-id="6a501-p101">Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="6a501-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a501-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a501-125">Remarks</span></span>

<span data-ttu-id="6a501-126">Cualquier componente de fecha  _en datetime_ o  _expresión_ se descarta.</span><span class="sxs-lookup"><span data-stu-id="6a501-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="6a501-127">Si  _falta datetime_ o no se puede convertir en un resultado válido, esta función devuelve un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6a501-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="6a501-128">error.</span><span class="sxs-lookup"><span data-stu-id="6a501-128">error.</span></span> 
  
<span data-ttu-id="6a501-129">La función TIMEVALUE también acepta un  valor numérico único para la expresión donde la parte decimal del resultado representa la fracción de un día desde la medianoche.</span><span class="sxs-lookup"><span data-stu-id="6a501-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6a501-130">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="6a501-130">Example 1</span></span>

<span data-ttu-id="6a501-131">TIMEVALUE("6:00 a.m.")</span><span class="sxs-lookup"><span data-stu-id="6a501-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="6a501-132">Devuelve el valor que representa las 6:30 a. m.</span><span class="sxs-lookup"><span data-stu-id="6a501-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6a501-133">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="6a501-133">Example 2</span></span>

<span data-ttu-id="6a501-134">TIMEVALUE("14:30")+4 eh.+30 em.</span><span class="sxs-lookup"><span data-stu-id="6a501-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="6a501-135">Devuelve el valor que representa las 19:00:00.</span><span class="sxs-lookup"><span data-stu-id="6a501-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6a501-136">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="6a501-136">Example 3</span></span>

<span data-ttu-id="6a501-137">TIMEVALUE("11 a.m., 1 de julio de 1997")</span><span class="sxs-lookup"><span data-stu-id="6a501-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="6a501-138">Devuelve el valor que representa las 11:00 a. m.</span><span class="sxs-lookup"><span data-stu-id="6a501-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="6a501-139">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="6a501-139">Example 4</span></span>

<span data-ttu-id="6a501-140">TIMEVALUE(0.6337)</span><span class="sxs-lookup"><span data-stu-id="6a501-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="6a501-141">Devuelve el valor que representa las 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="6a501-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="6a501-142">Ejemplo 5</span><span class="sxs-lookup"><span data-stu-id="6a501-142">Example 5</span></span>

<span data-ttu-id="6a501-143">TIMEVALUE("7:89")</span><span class="sxs-lookup"><span data-stu-id="6a501-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="6a501-p103">Devuelve el error #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6a501-p103">Returns a #VALUE! error.</span></span>
  

