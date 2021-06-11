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
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433559"
---
# <a name="cy-function"></a><span data-ttu-id="2b0c8-103">Función CY</span><span class="sxs-lookup"><span data-stu-id="2b0c8-103">CY Function</span></span>

<span data-ttu-id="2b0c8-104">Devuelve un valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2b0c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b0c8-105">Syntax</span></span>

<span data-ttu-id="2b0c8-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2b0c8-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2b0c8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b0c8-107">Parameters</span></span>

|<span data-ttu-id="2b0c8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2b0c8-108">**Name**</span></span>|<span data-ttu-id="2b0c8-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="2b0c8-109">**Required/Optional**</span></span>|<span data-ttu-id="2b0c8-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="2b0c8-110">**Data Type**</span></span>|<span data-ttu-id="2b0c8-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2b0c8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2b0c8-112">_value_</span><span class="sxs-lookup"><span data-stu-id="2b0c8-112">_value_</span></span> <br/> |<span data-ttu-id="2b0c8-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="2b0c8-113">Optional</span></span>  <br/> |<span data-ttu-id="2b0c8-114">**Número o cadena**</span><span class="sxs-lookup"><span data-stu-id="2b0c8-114">**Number or String**</span></span> <br/> |<span data-ttu-id="2b0c8-115">Número o cadena que incluye formato específico de moneda.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="2b0c8-116">Si no se especifica, el valor de moneda tiene el formato de acuerdo con el estilo de moneda en la configuración región e idioma del sistema.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="2b0c8-117">_cyID_</span><span class="sxs-lookup"><span data-stu-id="2b0c8-117">_cyID_</span></span> <br/> |<span data-ttu-id="2b0c8-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="2b0c8-118">Optional</span></span>  <br/> |<span data-ttu-id="2b0c8-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="2b0c8-119">**Number**</span></span> <br/> |<span data-ttu-id="2b0c8-120">Un identificador numérico de moneda o una cadena entrecomillada de tres caracteres para la abreviatura ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b0c8-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b0c8-121">Remarks</span></span>

<span data-ttu-id="2b0c8-122">Para especificar una moneda diferente, debe incluir un _cyID válido._</span><span class="sxs-lookup"><span data-stu-id="2b0c8-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="2b0c8-123">Para ver una lista, vea [Constantes de moneda](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2b0c8-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="2b0c8-124">Si  _el_ valor es incompatible con el tipo de moneda designado, o si se especifica un argumento no válido como "no es un número", se #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2b0c8-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="2b0c8-125">error se devuelve.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-125">error is returned.</span></span> <span data-ttu-id="2b0c8-126">Si  _el_ valor es mayor que 922.337.203.685.477.5807 o inferior a -922.337.203.685.477.5808, un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2b0c8-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="2b0c8-127">error se devuelve.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-127">error is returned.</span></span> 
  
<span data-ttu-id="2b0c8-128">Para obtener una mayor precisión con valores de moneda muy grandes que incluyen fracciones de una unidad, como 3,6 trillones, use argumentos de cadena para  _el valor_.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="2b0c8-129">Especificar un  _cyID no válido_ devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="2b0c8-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="2b0c8-130">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b0c8-130">Example 1</span></span>

<span data-ttu-id="2b0c8-131">Si la configuración regional y de idioma del usuario especifica dólares estadounidenses:</span><span class="sxs-lookup"><span data-stu-id="2b0c8-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="2b0c8-132">CY(999998.993)</span><span class="sxs-lookup"><span data-stu-id="2b0c8-132">CY(999998.993)</span></span>
  
<span data-ttu-id="2b0c8-133">Devuelve $999.998,99</span><span class="sxs-lookup"><span data-stu-id="2b0c8-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="2b0c8-134">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="2b0c8-134">Example 2</span></span>

<span data-ttu-id="2b0c8-135">CY(12345678,993; "USD")</span><span class="sxs-lookup"><span data-stu-id="2b0c8-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="2b0c8-136">Devuelve $12.345.678,99</span><span class="sxs-lookup"><span data-stu-id="2b0c8-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="2b0c8-137">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="2b0c8-137">Example 3</span></span>

<span data-ttu-id="2b0c8-138">CY(12345678,993; "DEM")</span><span class="sxs-lookup"><span data-stu-id="2b0c8-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="2b0c8-139">Devuelve 12.345.678,99 DEM</span><span class="sxs-lookup"><span data-stu-id="2b0c8-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="2b0c8-140">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="2b0c8-140">Example 4</span></span>

<span data-ttu-id="2b0c8-141">CY(12345678,7832; "XXX")</span><span class="sxs-lookup"><span data-stu-id="2b0c8-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="2b0c8-142">Devuelve 12.345.678,78</span><span class="sxs-lookup"><span data-stu-id="2b0c8-142">Returns 12,345,678.78</span></span>
  

