---
title: Función DAY (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Devuelve un entero entre 1 y 31, que representa el día y hora o de expresión. La función día usa el calendario gregoriano.
ms.openlocfilehash: 07607b809aec9f50ae8981476313fc5e8dbc3423
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821952"
---
# <a name="day-function-visioshapesheet"></a><span data-ttu-id="9b2d6-104">Función DAY (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="9b2d6-104">DAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="9b2d6-105">Devuelve un entero entre 1 y 31, que representa el día _y hora_ o de _expresión_.</span><span class="sxs-lookup"><span data-stu-id="9b2d6-105">Returns an integer, 1 to 31, representing the day in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="9b2d6-106">La función día usa el calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="9b2d6-106">The DAY function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9b2d6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b2d6-107">Syntax</span></span>

<span data-ttu-id="9b2d6-108">DÍA ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="9b2d6-108">DAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9b2d6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b2d6-109">Parameters</span></span>

|<span data-ttu-id="9b2d6-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="9b2d6-110">**Name**</span></span>|<span data-ttu-id="9b2d6-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="9b2d6-111">**Required/Optional**</span></span>|<span data-ttu-id="9b2d6-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="9b2d6-112">**Data Type**</span></span>|<span data-ttu-id="9b2d6-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9b2d6-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9b2d6-114">_fecha y hora_</span><span class="sxs-lookup"><span data-stu-id="9b2d6-114">_datetime_</span></span> <br/> |<span data-ttu-id="9b2d6-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9b2d6-115">Required</span></span>  <br/> |<span data-ttu-id="9b2d6-116">**String**</span><span class="sxs-lookup"><span data-stu-id="9b2d6-116">**String**</span></span> <br/> |<span data-ttu-id="9b2d6-117">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="9b2d6-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="9b2d6-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="9b2d6-118">_expression_</span></span> <br/> |<span data-ttu-id="9b2d6-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9b2d6-119">Required</span></span>  <br/> |<span data-ttu-id="9b2d6-120">**String**</span><span class="sxs-lookup"><span data-stu-id="9b2d6-120">**String**</span></span> <br/> |<span data-ttu-id="9b2d6-121">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="9b2d6-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="9b2d6-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="9b2d6-122">_lcid_</span></span> <br/> |<span data-ttu-id="9b2d6-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="9b2d6-123">Optional</span></span>  <br/> |<span data-ttu-id="9b2d6-124">**Número**</span><span class="sxs-lookup"><span data-stu-id="9b2d6-124">**Number**</span></span> <br/> |<span data-ttu-id="9b2d6-p103">Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="9b2d6-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9b2d6-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b2d6-127">Return value</span></span>

<span data-ttu-id="9b2d6-128">Entero</span><span class="sxs-lookup"><span data-stu-id="9b2d6-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9b2d6-129">Notas</span><span class="sxs-lookup"><span data-stu-id="9b2d6-129">Remarks</span></span>

<span data-ttu-id="9b2d6-130">Se descarta cualquier componente de hora _y hora_ o de _expresión_ .</span><span class="sxs-lookup"><span data-stu-id="9b2d6-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="9b2d6-131">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="9b2d6-131">No rounding is done.</span></span> <span data-ttu-id="9b2d6-132">Si falta _fecha y hora_ o si no se puede convertir en un resultado válido, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="9b2d6-132">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="9b2d6-133">La función DAY también acepta un único valor numérico en _expresión_ , donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899.</span><span class="sxs-lookup"><span data-stu-id="9b2d6-133">The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="9b2d6-134">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b2d6-134">Example 1</span></span>

<span data-ttu-id="9b2d6-135">DAY("May 30, 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="9b2d6-135">DAY("May 30, 1997 15:45:24")</span></span>
  
<span data-ttu-id="9b2d6-136">Devuelve 30.</span><span class="sxs-lookup"><span data-stu-id="9b2d6-136">Returns 30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9b2d6-137">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="9b2d6-137">Example 2</span></span>

<span data-ttu-id="9b2d6-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="9b2d6-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="9b2d6-139">Devuelve 6.</span><span class="sxs-lookup"><span data-stu-id="9b2d6-139">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="9b2d6-140">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="9b2d6-140">Example 3</span></span>

<span data-ttu-id="9b2d6-141">DAY(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="9b2d6-141">DAY(35580.6337)</span></span>
  
<span data-ttu-id="9b2d6-142">Devuelve 30.</span><span class="sxs-lookup"><span data-stu-id="9b2d6-142">Returns 30.</span></span>
  

