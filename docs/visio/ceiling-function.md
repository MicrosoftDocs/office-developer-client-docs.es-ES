---
title: CEILING (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Redondea un número del valor 0 (cero) a la siguiente instancia de Multiple. Si no se especifica el múltiplo, el número se redondea alejándose del 0 al siguiente entero.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404130"
---
# <a name="ceiling-function"></a><span data-ttu-id="781d4-104">Función CEILING</span><span class="sxs-lookup"><span data-stu-id="781d4-104">CEILING Function</span></span>

<span data-ttu-id="781d4-105">Redondea un número del valor 0 (cero) a la siguiente instancia de _Multiple_.</span><span class="sxs-lookup"><span data-stu-id="781d4-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="781d4-106">Si no se especifica el _múltiplo_ , el número se redondea alejándose del 0 al siguiente entero.</span><span class="sxs-lookup"><span data-stu-id="781d4-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="781d4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="781d4-107">Syntax</span></span>

<span data-ttu-id="781d4-108">CEILING (\* \* *número* \* \*, \* \* *varios* \* \*)</span><span class="sxs-lookup"><span data-stu-id="781d4-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="781d4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="781d4-109">Parameters</span></span>

|<span data-ttu-id="781d4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="781d4-110">**Name**</span></span>|<span data-ttu-id="781d4-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="781d4-111">**Required/Optional**</span></span>|<span data-ttu-id="781d4-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="781d4-112">**Data Type**</span></span>|<span data-ttu-id="781d4-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="781d4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="781d4-114">_number_</span><span class="sxs-lookup"><span data-stu-id="781d4-114">_number_</span></span> <br/> |<span data-ttu-id="781d4-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="781d4-115">Required</span></span>  <br/> |<span data-ttu-id="781d4-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="781d4-116">**Number**</span></span> <br/> |<span data-ttu-id="781d4-117">El número que desea redondear.</span><span class="sxs-lookup"><span data-stu-id="781d4-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="781d4-118">_distintos_</span><span class="sxs-lookup"><span data-stu-id="781d4-118">_multiple_</span></span> <br/> |<span data-ttu-id="781d4-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="781d4-119">Required</span></span>  <br/> |<span data-ttu-id="781d4-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="781d4-120">**Number**</span></span> <br/> |<span data-ttu-id="781d4-121">Múltiplo al que se va a redondear.</span><span class="sxs-lookup"><span data-stu-id="781d4-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="781d4-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="781d4-122">Remarks</span></span>

 <span data-ttu-id="781d4-123">_Número_ y _varios_ deben tener los mismos signos o un #NUM!</span><span class="sxs-lookup"><span data-stu-id="781d4-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="781d4-124">se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="781d4-124">error is returned.</span></span> <span data-ttu-id="781d4-125">Si uno o _varios_ _números_ no se pueden convertir en un valor, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="781d4-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="781d4-126">se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="781d4-126">error is returned.</span></span> <span data-ttu-id="781d4-127">Si _número_ o _múltiplo_ es 0, el resultado es 0.</span><span class="sxs-lookup"><span data-stu-id="781d4-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="781d4-128">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="781d4-128">Example 1</span></span>

<span data-ttu-id="781d4-129">TECHO (3.7)</span><span class="sxs-lookup"><span data-stu-id="781d4-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="781d4-130">Devuelve 4.</span><span class="sxs-lookup"><span data-stu-id="781d4-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="781d4-131">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="781d4-131">Example 2</span></span>

<span data-ttu-id="781d4-132">TECHO (-3,7)</span><span class="sxs-lookup"><span data-stu-id="781d4-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="781d4-133">Devuelve -4.</span><span class="sxs-lookup"><span data-stu-id="781d4-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="781d4-134">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="781d4-134">Example 3</span></span>

<span data-ttu-id="781d4-135">CEILING (3,7, 0,25)</span><span class="sxs-lookup"><span data-stu-id="781d4-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="781d4-136">Devuelve 3,75.</span><span class="sxs-lookup"><span data-stu-id="781d4-136">Returns 3.75</span></span>
  

