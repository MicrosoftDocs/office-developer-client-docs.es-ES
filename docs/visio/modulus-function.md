---
title: MODULUS (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Devuelve el resto (módulo) que se produce cuando un número se divide por un divisor.
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429274"
---
# <a name="modulus-function"></a><span data-ttu-id="20e69-103">Función MODULUS</span><span class="sxs-lookup"><span data-stu-id="20e69-103">MODULUS Function</span></span>

<span data-ttu-id="20e69-104">Devuelve el resto (módulo) que se produce cuando un número se divide por un divisor.</span><span class="sxs-lookup"><span data-stu-id="20e69-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="20e69-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20e69-105">Syntax</span></span>

<span data-ttu-id="20e69-106">MODULUS(\*\* *number* \*\*, \*\* *divisor* \*\* )</span><span class="sxs-lookup"><span data-stu-id="20e69-106">MODULUS(\*\* *number* \*\*, \*\* *divisor* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="20e69-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20e69-107">Parameters</span></span>

|<span data-ttu-id="20e69-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="20e69-108">**Name**</span></span>|<span data-ttu-id="20e69-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="20e69-109">**Required/Optional**</span></span>|<span data-ttu-id="20e69-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="20e69-110">**Data Type**</span></span>|<span data-ttu-id="20e69-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20e69-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="20e69-112">_number_</span><span class="sxs-lookup"><span data-stu-id="20e69-112">_number_</span></span> <br/> |<span data-ttu-id="20e69-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="20e69-113">Required</span></span>  <br/> |<span data-ttu-id="20e69-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="20e69-114">**Number**</span></span> <br/> |<span data-ttu-id="20e69-115">El dividendo.</span><span class="sxs-lookup"><span data-stu-id="20e69-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="20e69-116">_divisor_</span><span class="sxs-lookup"><span data-stu-id="20e69-116">_divisor_</span></span> <br/> |<span data-ttu-id="20e69-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="20e69-117">Required</span></span>  <br/> |<span data-ttu-id="20e69-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="20e69-118">**Number**</span></span> <br/> |<span data-ttu-id="20e69-119">El divisor.</span><span class="sxs-lookup"><span data-stu-id="20e69-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="20e69-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20e69-120">Return value</span></span>

<span data-ttu-id="20e69-121">Número</span><span class="sxs-lookup"><span data-stu-id="20e69-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20e69-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20e69-122">Remarks</span></span>

<span data-ttu-id="20e69-p101">El resultado tiene el mismo signo que el divisor. Se devuelve el error #DIV/0! cuando el divisor vale 0.</span><span class="sxs-lookup"><span data-stu-id="20e69-p101">The result has the same sign as the divisor. A #DIV/0! error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="20e69-126">En casi todas las ocasiones es aconsejable utilizar la función MODULUS en lugar de la función MOD.</span><span class="sxs-lookup"><span data-stu-id="20e69-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="20e69-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="20e69-127">Example 1</span></span>

<span data-ttu-id="20e69-128">MODULUS(5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="20e69-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="20e69-129">Devuelve 0,8.</span><span class="sxs-lookup"><span data-stu-id="20e69-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="20e69-130">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="20e69-130">Example 2</span></span>

<span data-ttu-id="20e69-131">MODULUS(5, -1.4)</span><span class="sxs-lookup"><span data-stu-id="20e69-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="20e69-132">Devuelve -0,6.</span><span class="sxs-lookup"><span data-stu-id="20e69-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="20e69-133">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="20e69-133">Example 3</span></span>

<span data-ttu-id="20e69-134">MODULUS(-5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="20e69-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="20e69-135">Devuelve 0,6.</span><span class="sxs-lookup"><span data-stu-id="20e69-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="20e69-136">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="20e69-136">Example 4</span></span>

<span data-ttu-id="20e69-137">MODULUS(-5, -1.4)</span><span class="sxs-lookup"><span data-stu-id="20e69-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="20e69-138">Devuelve -0,8.</span><span class="sxs-lookup"><span data-stu-id="20e69-138">Returns -0.8.</span></span>
  

