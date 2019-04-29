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
description: Devuelve el valor de hora representado por fechaHora o expresión, en función de la configuración regional y de idioma del sistema.
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432327"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="abbf8-103">Función TIMEVALUE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="abbf8-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="abbf8-104">Devuelve el valor de hora representado por _fechaHora_ o _expresión_, en función de la configuración regional y de idioma del sistema.</span><span class="sxs-lookup"><span data-stu-id="abbf8-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="abbf8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abbf8-105">Syntax</span></span>

<span data-ttu-id="abbf8-106">TIMEVALUE ("\* \* *fecha y hora* \* \*" | \* \* *expresión* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="abbf8-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="abbf8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abbf8-107">Parameters</span></span>

|<span data-ttu-id="abbf8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="abbf8-108">**Name**</span></span>|<span data-ttu-id="abbf8-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="abbf8-109">**Required/Optional**</span></span>|<span data-ttu-id="abbf8-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="abbf8-110">**Data Type**</span></span>|<span data-ttu-id="abbf8-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="abbf8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="abbf8-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="abbf8-112">_datetime_</span></span> <br/> |<span data-ttu-id="abbf8-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="abbf8-113">Required</span></span>  <br/> |<span data-ttu-id="abbf8-114">**String**</span><span class="sxs-lookup"><span data-stu-id="abbf8-114">**String**</span></span> <br/> | <span data-ttu-id="abbf8-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="abbf8-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="abbf8-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="abbf8-116">_expression_</span></span> <br/> |<span data-ttu-id="abbf8-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="abbf8-117">Required</span></span>  <br/> |<span data-ttu-id="abbf8-118">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="abbf8-118">**Varies**</span></span> <br/> | <span data-ttu-id="abbf8-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="abbf8-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="abbf8-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="abbf8-120">_lcid_</span></span> <br/> |<span data-ttu-id="abbf8-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="abbf8-121">Optional</span></span>  <br/> |<span data-ttu-id="abbf8-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="abbf8-122">**Number**</span></span> <br/> |<span data-ttu-id="abbf8-123">Identificador regional que se usa para evaluar información de fecha y hora que no sea local.</span><span class="sxs-lookup"><span data-stu-id="abbf8-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="abbf8-124">El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="abbf8-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abbf8-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="abbf8-125">Remarks</span></span>

<span data-ttu-id="abbf8-126">Se descarta cualquier parte de fecha y _hora_ o de _expresión_ de un componente de fecha.</span><span class="sxs-lookup"><span data-stu-id="abbf8-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="abbf8-127">Si falta _fecha y hora_ o no se puede convertir en un resultado válido, la función devuelve un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="abbf8-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="abbf8-128">error.</span><span class="sxs-lookup"><span data-stu-id="abbf8-128">error.</span></span> 
  
<span data-ttu-id="abbf8-129">La función TIMEVALUE también acepta un único valor numérico en _expresión_ , en el que la parte decimal del resultado representa la fracción de un día contada a partir de la medianoche.</span><span class="sxs-lookup"><span data-stu-id="abbf8-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="abbf8-130">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="abbf8-130">Example 1</span></span>

<span data-ttu-id="abbf8-131">TIMEVALUE("6:00 a.m.")</span><span class="sxs-lookup"><span data-stu-id="abbf8-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="abbf8-132">Devuelve el valor que representa las 6:30 a. m.</span><span class="sxs-lookup"><span data-stu-id="abbf8-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="abbf8-133">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="abbf8-133">Example 2</span></span>

<span data-ttu-id="abbf8-134">TIMEVALUE("14:30")+4 eh.+30 em.</span><span class="sxs-lookup"><span data-stu-id="abbf8-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="abbf8-135">Devuelve el valor que representa las 19:00:00.</span><span class="sxs-lookup"><span data-stu-id="abbf8-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="abbf8-136">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="abbf8-136">Example 3</span></span>

<span data-ttu-id="abbf8-137">TIMEVALUE("11 a.m., 1 de julio de 1997")</span><span class="sxs-lookup"><span data-stu-id="abbf8-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="abbf8-138">Devuelve el valor que representa las 11:00 a. m.</span><span class="sxs-lookup"><span data-stu-id="abbf8-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="abbf8-139">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="abbf8-139">Example 4</span></span>

<span data-ttu-id="abbf8-140">TIMEVALUE (0.6337)</span><span class="sxs-lookup"><span data-stu-id="abbf8-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="abbf8-141">Devuelve el valor que representa las 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="abbf8-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="abbf8-142">Ejemplo 5</span><span class="sxs-lookup"><span data-stu-id="abbf8-142">Example 5</span></span>

<span data-ttu-id="abbf8-143">TIMEVALUE ("7:89")</span><span class="sxs-lookup"><span data-stu-id="abbf8-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="abbf8-p103">Devuelve el error #VALUE!</span><span class="sxs-lookup"><span data-stu-id="abbf8-p103">Returns a #VALUE! error.</span></span>
  

