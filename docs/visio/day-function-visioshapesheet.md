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
description: Devuelve un número entero, de 1 a 31, que representa el día en datetime o expresión. La función DAY usa el calendario gregoriano.
ms.openlocfilehash: 49c29d5dc25bf11599f89a20cb2bc2367bd74187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360301"
---
# <a name="day-function-visioshapesheet"></a><span data-ttu-id="a5fbb-104">Función DAY (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a5fbb-104">DAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a5fbb-105">Devuelve un número entero, de 1 a 31, que representa el día en  _datetime o_  _expresión_.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-105">Returns an integer, 1 to 31, representing the day in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="a5fbb-106">La función DAY usa el calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-106">The DAY function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a5fbb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5fbb-107">Syntax</span></span>

<span data-ttu-id="a5fbb-108">DAY(" \*\* *datetime* \*\* "| \*\* *expresión* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="a5fbb-108">DAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a5fbb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5fbb-109">Parameters</span></span>

|<span data-ttu-id="a5fbb-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a5fbb-110">**Name**</span></span>|<span data-ttu-id="a5fbb-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="a5fbb-111">**Required/Optional**</span></span>|<span data-ttu-id="a5fbb-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a5fbb-112">**Data Type**</span></span>|<span data-ttu-id="a5fbb-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5fbb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a5fbb-114">_datetime_</span><span class="sxs-lookup"><span data-stu-id="a5fbb-114">_datetime_</span></span> <br/> |<span data-ttu-id="a5fbb-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a5fbb-115">Required</span></span>  <br/> |<span data-ttu-id="a5fbb-116">**String**</span><span class="sxs-lookup"><span data-stu-id="a5fbb-116">**String**</span></span> <br/> |<span data-ttu-id="a5fbb-117">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="a5fbb-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="a5fbb-118">_expression_</span></span> <br/> |<span data-ttu-id="a5fbb-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a5fbb-119">Required</span></span>  <br/> |<span data-ttu-id="a5fbb-120">**String**</span><span class="sxs-lookup"><span data-stu-id="a5fbb-120">**String**</span></span> <br/> |<span data-ttu-id="a5fbb-121">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="a5fbb-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="a5fbb-122">_lcid_</span></span> <br/> |<span data-ttu-id="a5fbb-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="a5fbb-123">Optional</span></span>  <br/> |<span data-ttu-id="a5fbb-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="a5fbb-124">**Number**</span></span> <br/> |<span data-ttu-id="a5fbb-p103">Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a5fbb-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5fbb-127">Return value</span></span>

<span data-ttu-id="a5fbb-128">Entero</span><span class="sxs-lookup"><span data-stu-id="a5fbb-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5fbb-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5fbb-129">Remarks</span></span>

<span data-ttu-id="a5fbb-130">Cualquier componente de hora  _en datetime_ o  _expresión_ se descarta.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="a5fbb-131">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-131">No rounding is done.</span></span> <span data-ttu-id="a5fbb-132">Si  _falta datetime_ o no se puede convertir en un resultado válido, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-132">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="a5fbb-133">La función DAY también acepta un  valor de número único para la expresión donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-133">The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a5fbb-134">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5fbb-134">Example 1</span></span>

<span data-ttu-id="a5fbb-135">DAY("May 30, 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="a5fbb-135">DAY("May 30, 1997 15:45:24")</span></span>
  
<span data-ttu-id="a5fbb-136">Devuelve 30.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-136">Returns 30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a5fbb-137">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="a5fbb-137">Example 2</span></span>

<span data-ttu-id="a5fbb-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span><span class="sxs-lookup"><span data-stu-id="a5fbb-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="a5fbb-139">Devuelve 6.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-139">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a5fbb-140">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="a5fbb-140">Example 3</span></span>

<span data-ttu-id="a5fbb-141">DAY(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="a5fbb-141">DAY(35580.6337)</span></span>
  
<span data-ttu-id="a5fbb-142">Devuelve 30.</span><span class="sxs-lookup"><span data-stu-id="a5fbb-142">Returns 30.</span></span>
  

