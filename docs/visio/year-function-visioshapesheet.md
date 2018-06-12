---
title: Función YEAR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Devuelve un valor de tipo integer que representa el año gregoriano de fecha y hora o expresión, con formato de acuerdo con el estilo corto de fecha establecido en configuración de idioma y región actual del sistema.
ms.openlocfilehash: aaa183730440857d8d283912f4afeb3117ef737f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823600"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="51ab3-103">Función YEAR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="51ab3-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="51ab3-104">Devuelve un valor de tipo integer que representa el año gregoriano de _fecha y hora_ o _expresión_, con formato de acuerdo con el estilo corto de fecha establecido en configuración de idioma y región actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="51ab3-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="51ab3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51ab3-105">Syntax</span></span>

<span data-ttu-id="51ab3-106">AÑO ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="51ab3-106">YEAR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="51ab3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51ab3-107">Parameters</span></span>

|<span data-ttu-id="51ab3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="51ab3-108">**Name**</span></span>|<span data-ttu-id="51ab3-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="51ab3-109">**Required/Optional**</span></span>|<span data-ttu-id="51ab3-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="51ab3-110">**Data Type**</span></span>|<span data-ttu-id="51ab3-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="51ab3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="51ab3-112">_fecha y hora_</span><span class="sxs-lookup"><span data-stu-id="51ab3-112">_datetime_</span></span> <br/> |<span data-ttu-id="51ab3-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="51ab3-113">Required</span></span>  <br/> |<span data-ttu-id="51ab3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="51ab3-114">**String**</span></span> <br/> | <span data-ttu-id="51ab3-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="51ab3-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="51ab3-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="51ab3-116">_expression_</span></span> <br/> |<span data-ttu-id="51ab3-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="51ab3-117">Required</span></span>  <br/> |<span data-ttu-id="51ab3-118">**Varía**</span><span class="sxs-lookup"><span data-stu-id="51ab3-118">**Varies**</span></span> <br/> |<span data-ttu-id="51ab3-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="51ab3-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="51ab3-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="51ab3-120">_lcid_</span></span> <br/> |<span data-ttu-id="51ab3-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="51ab3-121">Optional</span></span>  <br/> |<span data-ttu-id="51ab3-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="51ab3-122">**Numeric**</span></span> <br/> |<span data-ttu-id="51ab3-p101">Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="51ab3-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="51ab3-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51ab3-125">Return value</span></span>

<span data-ttu-id="51ab3-126">Entero</span><span class="sxs-lookup"><span data-stu-id="51ab3-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51ab3-127">Notas</span><span class="sxs-lookup"><span data-stu-id="51ab3-127">Remarks</span></span>

<span data-ttu-id="51ab3-128">Se descarta el componente de tiempo de _fecha y hora_ o de _expresión_ .</span><span class="sxs-lookup"><span data-stu-id="51ab3-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="51ab3-129">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="51ab3-129">No rounding is done.</span></span> <span data-ttu-id="51ab3-130">Si falta _fecha y hora_ o si no se puede interpretar como una fecha u hora válidas, año devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="51ab3-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="51ab3-131">La función YEAR también acepta un único valor numérico en _expresión_ , donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899.</span><span class="sxs-lookup"><span data-stu-id="51ab3-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="51ab3-132">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="51ab3-132">Example 1</span></span>

<span data-ttu-id="51ab3-133">YEAR("10/27/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="51ab3-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="51ab3-134">Devuelve 2007.</span><span class="sxs-lookup"><span data-stu-id="51ab3-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="51ab3-135">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="51ab3-135">Example 2</span></span>

<span data-ttu-id="51ab3-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="51ab3-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="51ab3-137">Devuelve 2007.</span><span class="sxs-lookup"><span data-stu-id="51ab3-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="51ab3-138">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="51ab3-138">Example 3</span></span>

<span data-ttu-id="51ab3-139">YEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="51ab3-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="51ab3-140">Devuelve 1997.</span><span class="sxs-lookup"><span data-stu-id="51ab3-140">Returns 1997.</span></span>
  

