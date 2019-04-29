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
description: Devuelve un entero que representa el año gregoriano en fechaHora o expresión, con formato de acuerdo con el estilo de fecha corta establecido en la configuración regional y de idioma actual del sistema.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420713"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="1d11c-103">Función YEAR (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="1d11c-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="1d11c-104">Devuelve un entero que representa el año gregoriano en _fechaHora_ o _expresión_, con formato de acuerdo con el estilo de fecha corta establecido en la configuración regional y de idioma actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="1d11c-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1d11c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d11c-105">Syntax</span></span>

<span data-ttu-id="1d11c-106">YEAR ("\* \* *DateTime* \* \*" | \* \* *expresión* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="1d11c-106">YEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1d11c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d11c-107">Parameters</span></span>

|<span data-ttu-id="1d11c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="1d11c-108">**Name**</span></span>|<span data-ttu-id="1d11c-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="1d11c-109">**Required/Optional**</span></span>|<span data-ttu-id="1d11c-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="1d11c-110">**Data Type**</span></span>|<span data-ttu-id="1d11c-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d11c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1d11c-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="1d11c-112">_datetime_</span></span> <br/> |<span data-ttu-id="1d11c-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1d11c-113">Required</span></span>  <br/> |<span data-ttu-id="1d11c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1d11c-114">**String**</span></span> <br/> | <span data-ttu-id="1d11c-115">Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="1d11c-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="1d11c-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="1d11c-116">_expression_</span></span> <br/> |<span data-ttu-id="1d11c-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="1d11c-117">Required</span></span>  <br/> |<span data-ttu-id="1d11c-118">**Diferencias**</span><span class="sxs-lookup"><span data-stu-id="1d11c-118">**Varies**</span></span> <br/> |<span data-ttu-id="1d11c-119">Cualquier expresión que produzca como resultado una fecha y una hora.</span><span class="sxs-lookup"><span data-stu-id="1d11c-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="1d11c-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="1d11c-120">_lcid_</span></span> <br/> |<span data-ttu-id="1d11c-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="1d11c-121">Optional</span></span>  <br/> |<span data-ttu-id="1d11c-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="1d11c-122">**Numeric**</span></span> <br/> |<span data-ttu-id="1d11c-123">Identificador regional que se usa para evaluar información de fecha y hora que no sea local.</span><span class="sxs-lookup"><span data-stu-id="1d11c-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="1d11c-124">El identificador regional es un número que se describe en los archivos de encabezado del sistema.</span><span class="sxs-lookup"><span data-stu-id="1d11c-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1d11c-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d11c-125">Return value</span></span>

<span data-ttu-id="1d11c-126">Entero</span><span class="sxs-lookup"><span data-stu-id="1d11c-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d11c-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d11c-127">Remarks</span></span>

<span data-ttu-id="1d11c-128">Se descarta el componente de hora de _fecha_ y hora o de _expresión_ .</span><span class="sxs-lookup"><span data-stu-id="1d11c-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="1d11c-129">No se realiza redondeo.</span><span class="sxs-lookup"><span data-stu-id="1d11c-129">No rounding is done.</span></span> <span data-ttu-id="1d11c-130">Si falta _fechaHora_ o no se puede interpretar como una fecha u hora válidas, Year devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="1d11c-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="1d11c-131">La función YEAR también acepta un único valor numérico en _expresión_ , en el que la parte entera del resultado representa el número de días transcurridos desde el 30 de diciembre de 1899.</span><span class="sxs-lookup"><span data-stu-id="1d11c-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="1d11c-132">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="1d11c-132">Example 1</span></span>

<span data-ttu-id="1d11c-133">AÑO ("10/27/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="1d11c-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="1d11c-134">Devuelve 2007.</span><span class="sxs-lookup"><span data-stu-id="1d11c-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1d11c-135">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="1d11c-135">Example 2</span></span>

<span data-ttu-id="1d11c-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span><span class="sxs-lookup"><span data-stu-id="1d11c-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="1d11c-137">Devuelve 2007.</span><span class="sxs-lookup"><span data-stu-id="1d11c-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="1d11c-138">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="1d11c-138">Example 3</span></span>

<span data-ttu-id="1d11c-139">AÑO (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="1d11c-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="1d11c-140">Devuelve 1997.</span><span class="sxs-lookup"><span data-stu-id="1d11c-140">Returns 1997.</span></span>
  

