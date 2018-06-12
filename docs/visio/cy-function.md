---
title: CY (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
localization_priority: Normal
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: Devuelve un valor de moneda.
ms.openlocfilehash: ea7696e7628939466730b9c054a706a7a9fa264e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821890"
---
# <a name="cy-function"></a><span data-ttu-id="2ffbc-103">CY (función)</span><span class="sxs-lookup"><span data-stu-id="2ffbc-103">CY Function</span></span>

<span data-ttu-id="2ffbc-104">Devuelve un valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="2ffbc-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2ffbc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ffbc-105">Syntax</span></span>

<span data-ttu-id="2ffbc-106">CY (** *valor* **, ** *IdMoneda* **)</span><span class="sxs-lookup"><span data-stu-id="2ffbc-106">CY(** *value* **, ** *cyID* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2ffbc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ffbc-107">Parameters</span></span>

|<span data-ttu-id="2ffbc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2ffbc-108">**Name**</span></span>|<span data-ttu-id="2ffbc-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="2ffbc-109">**Required/Optional**</span></span>|<span data-ttu-id="2ffbc-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2ffbc-110">**Data Type**</span></span>|<span data-ttu-id="2ffbc-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2ffbc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2ffbc-112">_value_</span><span class="sxs-lookup"><span data-stu-id="2ffbc-112">_value_</span></span> <br/> |<span data-ttu-id="2ffbc-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="2ffbc-113">Optional</span></span>  <br/> |<span data-ttu-id="2ffbc-114">**Expresión numérica o cadena**</span><span class="sxs-lookup"><span data-stu-id="2ffbc-114">**Number or String**</span></span> <br/> |<span data-ttu-id="2ffbc-115">Un número o una cadena que incluye el formato específico de la moneda.</span><span class="sxs-lookup"><span data-stu-id="2ffbc-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="2ffbc-116">Si no se especifica, el valor de moneda tiene el formato según el estilo de moneda en la configuración del sistema regional y de idioma.</span><span class="sxs-lookup"><span data-stu-id="2ffbc-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="2ffbc-117">_IdMoneda_</span><span class="sxs-lookup"><span data-stu-id="2ffbc-117">_cyID_</span></span> <br/> |<span data-ttu-id="2ffbc-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="2ffbc-118">Optional</span></span>  <br/> |<span data-ttu-id="2ffbc-119">**Número**</span><span class="sxs-lookup"><span data-stu-id="2ffbc-119">**Number**</span></span> <br/> |<span data-ttu-id="2ffbc-120">Un ID de moneda numérica o una cadena entrecomillada de tres caracteres de la abreviatura de ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="2ffbc-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ffbc-121">Notas</span><span class="sxs-lookup"><span data-stu-id="2ffbc-121">Remarks</span></span>

<span data-ttu-id="2ffbc-122">Para especificar una moneda diferente, debe incluir un _IdMoneda_de válido.</span><span class="sxs-lookup"><span data-stu-id="2ffbc-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="2ffbc-123">Para obtener una lista, vea [acerca de las constantes de moneda](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2ffbc-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="2ffbc-124">Si el _valor_ no es compatible con el tipo de moneda designado, o si es un argumento no válido, como "no es un número" especificado, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2ffbc-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="2ffbc-125">se devuelve el error.</span><span class="sxs-lookup"><span data-stu-id="2ffbc-125">error is returned.</span></span> <span data-ttu-id="2ffbc-126">Si el _valor_ es mayor que 922.337.203.685.477,5807 o menor que -922.337.203.685.477,5808, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2ffbc-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="2ffbc-127">se devuelve el error.</span><span class="sxs-lookup"><span data-stu-id="2ffbc-127">error is returned.</span></span> 
  
<span data-ttu-id="2ffbc-128">Para mejorar la precisión con valores de moneda muy grandes que incluyan fracciones de unidad, como 3,6 billones, utilice argumentos de _valor de_cadena.</span><span class="sxs-lookup"><span data-stu-id="2ffbc-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="2ffbc-129">Especifica un _IdMoneda_ de no válido, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="2ffbc-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="2ffbc-130">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ffbc-130">Example 1</span></span>

<span data-ttu-id="2ffbc-131">Si la configuración regional y de idioma del usuario especifica dólares estadounidenses:</span><span class="sxs-lookup"><span data-stu-id="2ffbc-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="2ffbc-132">CY(999998.993)</span><span class="sxs-lookup"><span data-stu-id="2ffbc-132">CY(999998.993)</span></span>
  
<span data-ttu-id="2ffbc-133">Devuelve $999.998,99</span><span class="sxs-lookup"><span data-stu-id="2ffbc-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2ffbc-134">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="2ffbc-134">Example 2</span></span>

<span data-ttu-id="2ffbc-135">CY(12345678,993; "USD")</span><span class="sxs-lookup"><span data-stu-id="2ffbc-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="2ffbc-136">Devuelve $12.345.678,99</span><span class="sxs-lookup"><span data-stu-id="2ffbc-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="2ffbc-137">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="2ffbc-137">Example 3</span></span>

<span data-ttu-id="2ffbc-138">CY(12345678,993; "DEM")</span><span class="sxs-lookup"><span data-stu-id="2ffbc-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="2ffbc-139">Devuelve 12.345.678,99 DEM</span><span class="sxs-lookup"><span data-stu-id="2ffbc-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="2ffbc-140">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="2ffbc-140">Example 4</span></span>

<span data-ttu-id="2ffbc-141">CY(12345678,7832; "XXX")</span><span class="sxs-lookup"><span data-stu-id="2ffbc-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="2ffbc-142">Devuelve 12.345.678,78</span><span class="sxs-lookup"><span data-stu-id="2ffbc-142">Returns 12,345,678.78</span></span>
  

