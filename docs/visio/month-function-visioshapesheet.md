---
title: MONTH Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Devuelve un número entero de 1 a 12 que representa un mes.
ms.openlocfilehash: e17803a153b4aadec34aa751da7efa077963bba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822662"
---
# <a name="month-function-visioshapesheet"></a><span data-ttu-id="18cc4-103">MONTH Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="18cc4-103">MONTH Function (VisioShapeSheet)</span></span>

<span data-ttu-id="18cc4-104">Devuelve un número entero de 1 a 12 que representa un mes.</span><span class="sxs-lookup"><span data-stu-id="18cc4-104">Returns an integer from 1 to 12 that represents a month.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="18cc4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18cc4-105">Syntax</span></span>

<span data-ttu-id="18cc4-106">MONTH ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="18cc4-106">MONTH(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="18cc4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18cc4-107">Parameters</span></span>

|<span data-ttu-id="18cc4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="18cc4-108">**Name**</span></span>|<span data-ttu-id="18cc4-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="18cc4-109">**Required/Optional**</span></span>|<span data-ttu-id="18cc4-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="18cc4-110">**Data Type**</span></span>|<span data-ttu-id="18cc4-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18cc4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="18cc4-112">_fecha y hora_</span><span class="sxs-lookup"><span data-stu-id="18cc4-112">_datetime_</span></span> <br/> |<span data-ttu-id="18cc4-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="18cc4-113">Required</span></span>  <br/> |<span data-ttu-id="18cc4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="18cc4-114">**String**</span></span> <br/> |<span data-ttu-id="18cc4-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="18cc4-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="18cc4-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="18cc4-116">_expression_</span></span> <br/> |<span data-ttu-id="18cc4-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="18cc4-117">Required</span></span>  <br/> |<span data-ttu-id="18cc4-118">**String**</span><span class="sxs-lookup"><span data-stu-id="18cc4-118">**String**</span></span> <br/> | <span data-ttu-id="18cc4-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="18cc4-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="18cc4-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="18cc4-120">_lcid_</span></span> <br/> |<span data-ttu-id="18cc4-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="18cc4-121">Optional</span></span>  <br/> |<span data-ttu-id="18cc4-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="18cc4-122">**Number**</span></span> <br/> |<span data-ttu-id="18cc4-p101">Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="18cc4-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="18cc4-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18cc4-125">Return value</span></span>

<span data-ttu-id="18cc4-126">Entero</span><span class="sxs-lookup"><span data-stu-id="18cc4-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18cc4-127">Notas</span><span class="sxs-lookup"><span data-stu-id="18cc4-127">Remarks</span></span>

<span data-ttu-id="18cc4-128">El tiempo de _fecha y hora_ o de _expresión_ se descarta.</span><span class="sxs-lookup"><span data-stu-id="18cc4-128">The time component of  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="18cc4-p102">No se realiza redondeo. Si falta la cadena de entrada de datos o si ésta no se puede convertir en un valor válido, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="18cc4-p102">No rounding is done. If the input string is missing or cannot be converted to a valid result, the MONTH function returns an error.</span></span>
  
<span data-ttu-id="18cc4-131">El formato del valor devuelto corresponde al estilo corto de fecha establecido en la configuración regional actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="18cc4-131">The returned value is formatted according to the short date style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="18cc4-132">La función MONTH también acepta un único valor numérico en _expresión_ , donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899.</span><span class="sxs-lookup"><span data-stu-id="18cc4-132">The MONTH function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="18cc4-133">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="18cc4-133">Example 1</span></span>

<span data-ttu-id="18cc4-134">MONTH("May 30, 1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="18cc4-134">MONTH("May 30, 1999 13:45:24")</span></span>
  
<span data-ttu-id="18cc4-135">Devuelve 5.</span><span class="sxs-lookup"><span data-stu-id="18cc4-135">Returns 5.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="18cc4-136">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="18cc4-136">Example 2</span></span>

<span data-ttu-id="18cc4-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="18cc4-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span></span>
  
<span data-ttu-id="18cc4-138">Devuelve 6.</span><span class="sxs-lookup"><span data-stu-id="18cc4-138">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="18cc4-139">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="18cc4-139">Example 3</span></span>

<span data-ttu-id="18cc4-140">MONTH(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="18cc4-140">MONTH(35580.6337)</span></span>
  
<span data-ttu-id="18cc4-141">Devuelve 5.</span><span class="sxs-lookup"><span data-stu-id="18cc4-141">Returns 5.</span></span>
  

