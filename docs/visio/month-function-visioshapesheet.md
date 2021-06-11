---
title: Función MONTH (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Devuelve un entero de 1 a 12 que representa un mes.
ms.openlocfilehash: 71ecc7992839c871780e9b703377db37279246e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431977"
---
# <a name="month-function-visioshapesheet"></a><span data-ttu-id="ec456-103">Función MONTH (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="ec456-103">MONTH Function (VisioShapeSheet)</span></span>

<span data-ttu-id="ec456-104">Devuelve un entero de 1 a 12 que representa un mes.</span><span class="sxs-lookup"><span data-stu-id="ec456-104">Returns an integer from 1 to 12 that represents a month.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ec456-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec456-105">Syntax</span></span>

<span data-ttu-id="ec456-106">MONTH(" \*\* *datetime* \*\* "| \*\* *expresión* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="ec456-106">MONTH(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ec456-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec456-107">Parameters</span></span>

|<span data-ttu-id="ec456-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ec456-108">**Name**</span></span>|<span data-ttu-id="ec456-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="ec456-109">**Required/Optional**</span></span>|<span data-ttu-id="ec456-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ec456-110">**Data Type**</span></span>|<span data-ttu-id="ec456-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ec456-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ec456-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="ec456-112">_datetime_</span></span> <br/> |<span data-ttu-id="ec456-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ec456-113">Required</span></span>  <br/> |<span data-ttu-id="ec456-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ec456-114">**String**</span></span> <br/> |<span data-ttu-id="ec456-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="ec456-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="ec456-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="ec456-116">_expression_</span></span> <br/> |<span data-ttu-id="ec456-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ec456-117">Required</span></span>  <br/> |<span data-ttu-id="ec456-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ec456-118">**String**</span></span> <br/> | <span data-ttu-id="ec456-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="ec456-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="ec456-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="ec456-120">_lcid_</span></span> <br/> |<span data-ttu-id="ec456-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="ec456-121">Optional</span></span>  <br/> |<span data-ttu-id="ec456-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="ec456-122">**Number**</span></span> <br/> |<span data-ttu-id="ec456-p101">Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="ec456-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ec456-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec456-125">Return value</span></span>

<span data-ttu-id="ec456-126">Entero</span><span class="sxs-lookup"><span data-stu-id="ec456-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec456-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ec456-127">Remarks</span></span>

<span data-ttu-id="ec456-128">Se descarta el componente de _hora de fecha_ y hora o expresión. </span><span class="sxs-lookup"><span data-stu-id="ec456-128">The time component of  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="ec456-p102">No se realiza redondeo. Si falta la cadena de entrada de datos o si ésta no se puede convertir en un valor válido, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="ec456-p102">No rounding is done. If the input string is missing or cannot be converted to a valid result, the MONTH function returns an error.</span></span>
  
<span data-ttu-id="ec456-131">El formato del valor devuelto corresponde al estilo corto de fecha establecido en la configuración regional actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="ec456-131">The returned value is formatted according to the short date style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="ec456-132">La función MONTH también acepta un  valor de número único para la expresión donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899.</span><span class="sxs-lookup"><span data-stu-id="ec456-132">The MONTH function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ec456-133">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec456-133">Example 1</span></span>

<span data-ttu-id="ec456-134">MONTH("May 30, 1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="ec456-134">MONTH("May 30, 1999 13:45:24")</span></span>
  
<span data-ttu-id="ec456-135">Devuelve 5.</span><span class="sxs-lookup"><span data-stu-id="ec456-135">Returns 5.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ec456-136">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ec456-136">Example 2</span></span>

<span data-ttu-id="ec456-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="ec456-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span></span>
  
<span data-ttu-id="ec456-138">Devuelve 6.</span><span class="sxs-lookup"><span data-stu-id="ec456-138">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ec456-139">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="ec456-139">Example 3</span></span>

<span data-ttu-id="ec456-140">MONTH(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="ec456-140">MONTH(35580.6337)</span></span>
  
<span data-ttu-id="ec456-141">Devuelve 5.</span><span class="sxs-lookup"><span data-stu-id="ec456-141">Returns 5.</span></span>
  

