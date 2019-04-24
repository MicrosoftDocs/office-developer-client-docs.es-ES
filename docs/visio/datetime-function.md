---
title: DATETIME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
localization_priority: Normal
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: Devuelve el valor de fecha y hora representado por fechaHora o expresión.
ms.openlocfilehash: 2da084f685c044d48495b04f727a877140b51004
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360322"
---
# <a name="datetime-function"></a><span data-ttu-id="4177a-103">Función DATETIME</span><span class="sxs-lookup"><span data-stu-id="4177a-103">DATETIME Function</span></span>

<span data-ttu-id="4177a-104">Devuelve el valor de fecha y hora representado por _fechaHora_ o _expresión_.</span><span class="sxs-lookup"><span data-stu-id="4177a-104">Returns the date and time value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4177a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4177a-105">Syntax</span></span>

<span data-ttu-id="4177a-106">DATETIME ("\* \* *DateTime* \* \*" | \* \* *expresión* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="4177a-106">DATETIME(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4177a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4177a-107">Parameters</span></span>

|<span data-ttu-id="4177a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4177a-108">**Name**</span></span>|<span data-ttu-id="4177a-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="4177a-109">**Required/Optional**</span></span>|<span data-ttu-id="4177a-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="4177a-110">**Data Type**</span></span>|<span data-ttu-id="4177a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4177a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4177a-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="4177a-112">_datetime_</span></span> <br/> |<span data-ttu-id="4177a-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4177a-113">Required</span></span>  <br/> |<span data-ttu-id="4177a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4177a-114">**String**</span></span> <br/> |<span data-ttu-id="4177a-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="4177a-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="4177a-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="4177a-116">_expression_</span></span> <br/> |<span data-ttu-id="4177a-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4177a-117">Required</span></span>  <br/> |<span data-ttu-id="4177a-118">**String**</span><span class="sxs-lookup"><span data-stu-id="4177a-118">**String**</span></span> <br/> |<span data-ttu-id="4177a-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="4177a-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="4177a-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="4177a-120">_lcid_</span></span> <br/> |<span data-ttu-id="4177a-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="4177a-121">Optional</span></span>  <br/> |<span data-ttu-id="4177a-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="4177a-122">**Number**</span></span> <br/> |<span data-ttu-id="4177a-p101">Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="4177a-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4177a-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4177a-125">Return value</span></span>

<span data-ttu-id="4177a-126">DateTime</span><span class="sxs-lookup"><span data-stu-id="4177a-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4177a-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4177a-127">Remarks</span></span>

<span data-ttu-id="4177a-128">Si falta *fechaHora* o no se puede interpretar como una fecha u hora válidas, DateTime devuelve un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="4177a-128">If  *datetime*  is missing or cannot be interpreted as a valid date or time, DATETIME returns a #VALUE!</span></span> <span data-ttu-id="4177a-129">error.</span><span class="sxs-lookup"><span data-stu-id="4177a-129">error.</span></span> 
  
<span data-ttu-id="4177a-130">El formato del valor devuelto corresponde al estilo corto de fecha y hora establecido en la configuración regional actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="4177a-130">The returned value is formatted according to the short date style and time style in the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="4177a-131">La función DATETIME también acepta un único valor numérico en *expresión* , en el que la parte entera del resultado representa el número de días transcurridos desde el 30 de diciembre de 1899, y la parte decimal representa la fracción de un día a partir de la medianoche.</span><span class="sxs-lookup"><span data-stu-id="4177a-131">The DATETIME function also accepts a single number value for  *expression*  where the integer portion of the result represents the number of days since December 30, 1899, and the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4177a-132">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="4177a-132">Example 1</span></span>

<span data-ttu-id="4177a-133">DATETIME("May 30, 1997")+5 ed.</span><span class="sxs-lookup"><span data-stu-id="4177a-133">DATETIME("May 30, 1997")+5 ed.</span></span>
  
<span data-ttu-id="4177a-134">Devuelve el valor que corresponde al 4/6/1997.</span><span class="sxs-lookup"><span data-stu-id="4177a-134">Returns the value representing 6/4/1997.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4177a-135">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="4177a-135">Example 2</span></span>

<span data-ttu-id="4177a-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span><span class="sxs-lookup"><span data-stu-id="4177a-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span></span>
  
<span data-ttu-id="4177a-137">Devuelve la cadena "martes, 20 de mayo de 1997, 2:30:45 p.m."</span><span class="sxs-lookup"><span data-stu-id="4177a-137">Returns the string "Tuesday, May 20, 1997 2:30:45 PM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4177a-138">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="4177a-138">Example 3</span></span>

<span data-ttu-id="4177a-139">DATETIME("1:30 p.m. 19 de julio")</span><span class="sxs-lookup"><span data-stu-id="4177a-139">DATETIME("1:30 PM July 19")</span></span>
  
<span data-ttu-id="4177a-140">Devuelve el valor que corresponde al 19/7/2001 1:30:00 p. m. (suponiendo que el año actual sea el 2001).</span><span class="sxs-lookup"><span data-stu-id="4177a-140">Returns the value representing 7/19/2001 1:30:00 PM (assuming the current year is 2001).</span></span>
  
## <a name="example-4"></a><span data-ttu-id="4177a-141">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="4177a-141">Example 4</span></span>

<span data-ttu-id="4177a-142">DATETIME (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="4177a-142">DATETIME(35580.6337)</span></span>
  
<span data-ttu-id="4177a-143">Devuelve el valor que corresponde al 30/5/1997 3:12:32 p. m.</span><span class="sxs-lookup"><span data-stu-id="4177a-143">Returns the value representing 5/30/1997 3:12:32 PM.</span></span>
  

