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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344992"
---
# <a name="cy-function"></a><span data-ttu-id="35809-103">Función CY</span><span class="sxs-lookup"><span data-stu-id="35809-103">CY Function</span></span>

<span data-ttu-id="35809-104">Devuelve un valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="35809-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="35809-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35809-105">Syntax</span></span>

<span data-ttu-id="35809-106">CY (\* \* *valor* \* \*, \* \* *idmoneda* \* \*)</span><span class="sxs-lookup"><span data-stu-id="35809-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="35809-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35809-107">Parameters</span></span>

|<span data-ttu-id="35809-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="35809-108">**Name**</span></span>|<span data-ttu-id="35809-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="35809-109">**Required/Optional**</span></span>|<span data-ttu-id="35809-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="35809-110">**Data Type**</span></span>|<span data-ttu-id="35809-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="35809-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="35809-112">_value_</span><span class="sxs-lookup"><span data-stu-id="35809-112">_value_</span></span> <br/> |<span data-ttu-id="35809-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="35809-113">Optional</span></span>  <br/> |<span data-ttu-id="35809-114">**Número o cadena**</span><span class="sxs-lookup"><span data-stu-id="35809-114">**Number or String**</span></span> <br/> |<span data-ttu-id="35809-115">Un número o una cadena que incluye el formato específico de moneda.</span><span class="sxs-lookup"><span data-stu-id="35809-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="35809-116">Si no se especifica, el valor de moneda tiene el formato de acuerdo con el estilo moneda de la configuración regional y de idioma del sistema.</span><span class="sxs-lookup"><span data-stu-id="35809-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="35809-117">_Idmoneda_</span><span class="sxs-lookup"><span data-stu-id="35809-117">_cyID_</span></span> <br/> |<span data-ttu-id="35809-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="35809-118">Optional</span></span>  <br/> |<span data-ttu-id="35809-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="35809-119">**Number**</span></span> <br/> |<span data-ttu-id="35809-120">Un identificador de moneda numérico o una cadena con comillas de tres caracteres para la abreviatura ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="35809-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35809-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35809-121">Remarks</span></span>

<span data-ttu-id="35809-122">Para especificar una moneda distinta, debe incluir una _idmoneda_válida.</span><span class="sxs-lookup"><span data-stu-id="35809-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="35809-123">Para ver una lista, vea [Constantes de moneda](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="35809-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="35809-124">Si el _valor_ es incompatible con el tipo de moneda designado o si se ha especificado un argumento no válido, como "no es un número", #VALUE!</span><span class="sxs-lookup"><span data-stu-id="35809-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="35809-125">se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="35809-125">error is returned.</span></span> <span data-ttu-id="35809-126">Si el _valor_ es mayor que 922.337.203.685.477,5807 o menor que-922.337.203.685.477,5808, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="35809-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="35809-127">se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="35809-127">error is returned.</span></span> 
  
<span data-ttu-id="35809-128">Para obtener una mayor precisión con valores de moneda muy grandes que incluyan fracciones de una unidad, como 3,6 billones, use argumentos de cadena para el _valor_.</span><span class="sxs-lookup"><span data-stu-id="35809-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="35809-129">Si se especifica un _idmoneda_ no válido, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="35809-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="35809-130">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="35809-130">Example 1</span></span>

<span data-ttu-id="35809-131">Si la configuración regional y de idioma del usuario especifica dólares estadounidenses:</span><span class="sxs-lookup"><span data-stu-id="35809-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="35809-132">CY (999998.993)</span><span class="sxs-lookup"><span data-stu-id="35809-132">CY(999998.993)</span></span>
  
<span data-ttu-id="35809-133">Devuelve $999.998,99</span><span class="sxs-lookup"><span data-stu-id="35809-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="35809-134">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="35809-134">Example 2</span></span>

<span data-ttu-id="35809-135">CY(12345678,993; "USD")</span><span class="sxs-lookup"><span data-stu-id="35809-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="35809-136">Devuelve $12.345.678,99</span><span class="sxs-lookup"><span data-stu-id="35809-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="35809-137">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="35809-137">Example 3</span></span>

<span data-ttu-id="35809-138">CY(12345678,993; "DEM")</span><span class="sxs-lookup"><span data-stu-id="35809-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="35809-139">Devuelve 12.345.678,99 DEM</span><span class="sxs-lookup"><span data-stu-id="35809-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="35809-140">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="35809-140">Example 4</span></span>

<span data-ttu-id="35809-141">CY(12345678,7832; "XXX")</span><span class="sxs-lookup"><span data-stu-id="35809-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="35809-142">Devuelve 12.345.678,78</span><span class="sxs-lookup"><span data-stu-id="35809-142">Returns 12,345,678.78</span></span>
  

