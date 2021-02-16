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
description: Redondear un número de 0 (cero) a la siguiente instancia de múltiplo. Si no se especifica multiple, el número se redondea de 0 al siguiente entero.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404130"
---
# <a name="ceiling-function"></a><span data-ttu-id="ce17e-104">Función CEILING</span><span class="sxs-lookup"><span data-stu-id="ce17e-104">CEILING Function</span></span>

<span data-ttu-id="ce17e-105">Redondea un número de 0 (cero) a la siguiente instancia de  _varios_.</span><span class="sxs-lookup"><span data-stu-id="ce17e-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="ce17e-106">Si  _no_ se especifica multiple, el número se redondea de 0 al siguiente entero.</span><span class="sxs-lookup"><span data-stu-id="ce17e-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ce17e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce17e-107">Syntax</span></span>

<span data-ttu-id="ce17e-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ce17e-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ce17e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce17e-109">Parameters</span></span>

|<span data-ttu-id="ce17e-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="ce17e-110">**Name**</span></span>|<span data-ttu-id="ce17e-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="ce17e-111">**Required/Optional**</span></span>|<span data-ttu-id="ce17e-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ce17e-112">**Data Type**</span></span>|<span data-ttu-id="ce17e-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce17e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ce17e-114">_number_</span><span class="sxs-lookup"><span data-stu-id="ce17e-114">_number_</span></span> <br/> |<span data-ttu-id="ce17e-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ce17e-115">Required</span></span>  <br/> |<span data-ttu-id="ce17e-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="ce17e-116">**Number**</span></span> <br/> |<span data-ttu-id="ce17e-117">El número que desea redondear.</span><span class="sxs-lookup"><span data-stu-id="ce17e-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="ce17e-118">_multiple_</span><span class="sxs-lookup"><span data-stu-id="ce17e-118">_multiple_</span></span> <br/> |<span data-ttu-id="ce17e-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ce17e-119">Required</span></span>  <br/> |<span data-ttu-id="ce17e-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="ce17e-120">**Number**</span></span> <br/> |<span data-ttu-id="ce17e-121">Múltiplo al que redondear.</span><span class="sxs-lookup"><span data-stu-id="ce17e-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce17e-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce17e-122">Remarks</span></span>

 <span data-ttu-id="ce17e-123">_El_ número  _y el_ múltiplo deben tener los mismos signos o un #NUM!</span><span class="sxs-lookup"><span data-stu-id="ce17e-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="ce17e-124">se devuelve.</span><span class="sxs-lookup"><span data-stu-id="ce17e-124">error is returned.</span></span> <span data-ttu-id="ce17e-125">Si no  _se_  _puede_ convertir un número o varios en un valor, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="ce17e-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="ce17e-126">se devuelve.</span><span class="sxs-lookup"><span data-stu-id="ce17e-126">error is returned.</span></span> <span data-ttu-id="ce17e-127">Si el  _número_ o  _múltiplo_ es 0, el resultado es 0.</span><span class="sxs-lookup"><span data-stu-id="ce17e-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ce17e-128">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce17e-128">Example 1</span></span>

<span data-ttu-id="ce17e-129">CEILING(3.7)</span><span class="sxs-lookup"><span data-stu-id="ce17e-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="ce17e-130">Devuelve 4.</span><span class="sxs-lookup"><span data-stu-id="ce17e-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ce17e-131">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce17e-131">Example 2</span></span>

<span data-ttu-id="ce17e-132">CEILING(-3.7)</span><span class="sxs-lookup"><span data-stu-id="ce17e-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="ce17e-133">Devuelve -4.</span><span class="sxs-lookup"><span data-stu-id="ce17e-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ce17e-134">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="ce17e-134">Example 3</span></span>

<span data-ttu-id="ce17e-135">CEILING(3.7, 0.25)</span><span class="sxs-lookup"><span data-stu-id="ce17e-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="ce17e-136">Devuelve 3,75.</span><span class="sxs-lookup"><span data-stu-id="ce17e-136">Returns 3.75</span></span>
  

