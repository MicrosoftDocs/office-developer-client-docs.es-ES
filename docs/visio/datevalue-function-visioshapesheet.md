---
title: Función DATEVALUE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Devuelve el valor de fecha representado por fecha y hora o expresión.
ms.openlocfilehash: 7fcfd625b5e4e3da71a1b160c074401b672e0be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821937"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="6b045-103">Función DATEVALUE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="6b045-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="6b045-104">Devuelve el valor de fecha representado por _fecha y hora_ o _expresión_.</span><span class="sxs-lookup"><span data-stu-id="6b045-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6b045-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b045-105">Syntax</span></span>

<span data-ttu-id="6b045-106">DATEVALUE ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="6b045-106">DATEVALUE(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6b045-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b045-107">Parameters</span></span>

|<span data-ttu-id="6b045-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6b045-108">**Name**</span></span>|<span data-ttu-id="6b045-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="6b045-109">**Required/Optional**</span></span>|<span data-ttu-id="6b045-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="6b045-110">**Data Type**</span></span>|<span data-ttu-id="6b045-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b045-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6b045-112">_fecha y hora_</span><span class="sxs-lookup"><span data-stu-id="6b045-112">_datetime_</span></span> <br/> |<span data-ttu-id="6b045-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6b045-113">Required</span></span>  <br/> |<span data-ttu-id="6b045-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6b045-114">**String**</span></span> <br/> |<span data-ttu-id="6b045-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="6b045-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="6b045-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="6b045-116">_expression_</span></span> <br/> |<span data-ttu-id="6b045-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6b045-117">Required</span></span>  <br/> |<span data-ttu-id="6b045-118">**String**</span><span class="sxs-lookup"><span data-stu-id="6b045-118">**String**</span></span> <br/> |<span data-ttu-id="6b045-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="6b045-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="6b045-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="6b045-120">_lcid_</span></span> <br/> |<span data-ttu-id="6b045-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="6b045-121">Optional</span></span>  <br/> |<span data-ttu-id="6b045-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="6b045-122">**Number**</span></span> <br/> |<span data-ttu-id="6b045-p101">Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="6b045-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6b045-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b045-125">Return value</span></span>

<span data-ttu-id="6b045-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="6b045-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b045-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b045-127">Remarks</span></span>

<span data-ttu-id="6b045-128">Se descarta cualquier componente de hora *y hora* o de *expresión* .</span><span class="sxs-lookup"><span data-stu-id="6b045-128">Any time component in  *datetime*  or  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="6b045-129">Si falta *fecha y hora* o si no se puede convertir en un resultado válido, esta función devuelve #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6b045-129">If  *datetime*  is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE!</span></span> <span data-ttu-id="6b045-130">error.</span><span class="sxs-lookup"><span data-stu-id="6b045-130">error.</span></span> 
  
<span data-ttu-id="6b045-131">El valor devuelto se muestra utilizando el estilo corto de fecha establecido en la configuración regional actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="6b045-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="6b045-132">La función DATEVALUE también acepta un único valor numérico en *expresión* , donde la parte entera del resultado representa los días transcurridos desde el 30 de diciembre de 1899.</span><span class="sxs-lookup"><span data-stu-id="6b045-132">The DATEVALUE function also accepts a single number value for  *expression*  where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6b045-133">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b045-133">Example 1</span></span>

<span data-ttu-id="6b045-134">DATEVALUE(NOW( ))+5 ed.</span><span class="sxs-lookup"><span data-stu-id="6b045-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="6b045-135">Devuelve la fecha que será dentro de cinco días.</span><span class="sxs-lookup"><span data-stu-id="6b045-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6b045-136">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="6b045-136">Example 2</span></span>

<span data-ttu-id="6b045-137">DATEVALUE("7/19/1995 12:30")</span><span class="sxs-lookup"><span data-stu-id="6b045-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="6b045-138">Devuelve la fecha.</span><span class="sxs-lookup"><span data-stu-id="6b045-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6b045-139">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="6b045-139">Example 3</span></span>

<span data-ttu-id="6b045-140">DATEVALUE("Mayo 33, 1997")</span><span class="sxs-lookup"><span data-stu-id="6b045-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="6b045-p103">Devuelve el error #VALUE!</span><span class="sxs-lookup"><span data-stu-id="6b045-p103">Returns a #VALUE! error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="6b045-143">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="6b045-143">Example 4</span></span>

<span data-ttu-id="6b045-144">DATEVALUE(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="6b045-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="6b045-145">Devuelve 30/5/1997.</span><span class="sxs-lookup"><span data-stu-id="6b045-145">Returns 5/30/1997.</span></span>
  

