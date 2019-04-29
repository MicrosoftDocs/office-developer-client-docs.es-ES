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
# <a name="modulus-function"></a><span data-ttu-id="03c73-103">Función MODULUS</span><span class="sxs-lookup"><span data-stu-id="03c73-103">MODULUS Function</span></span>

<span data-ttu-id="03c73-104">Devuelve el resto (módulo) que se produce cuando un número se divide por un divisor.</span><span class="sxs-lookup"><span data-stu-id="03c73-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="03c73-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03c73-105">Syntax</span></span>

<span data-ttu-id="03c73-106">MÓDULO (\* \* *número* \* \*, \* \* *Núm_divisor* \* \*)</span><span class="sxs-lookup"><span data-stu-id="03c73-106">MODULUS(\*\* *number* \*\*, \*\* *divisor* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="03c73-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03c73-107">Parameters</span></span>

|<span data-ttu-id="03c73-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="03c73-108">**Name**</span></span>|<span data-ttu-id="03c73-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="03c73-109">**Required/Optional**</span></span>|<span data-ttu-id="03c73-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="03c73-110">**Data Type**</span></span>|<span data-ttu-id="03c73-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="03c73-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="03c73-112">_number_</span><span class="sxs-lookup"><span data-stu-id="03c73-112">_number_</span></span> <br/> |<span data-ttu-id="03c73-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="03c73-113">Required</span></span>  <br/> |<span data-ttu-id="03c73-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="03c73-114">**Number**</span></span> <br/> |<span data-ttu-id="03c73-115">El dividendo.</span><span class="sxs-lookup"><span data-stu-id="03c73-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="03c73-116">_visor_</span><span class="sxs-lookup"><span data-stu-id="03c73-116">_divisor_</span></span> <br/> |<span data-ttu-id="03c73-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="03c73-117">Required</span></span>  <br/> |<span data-ttu-id="03c73-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="03c73-118">**Number**</span></span> <br/> |<span data-ttu-id="03c73-119">El divisor.</span><span class="sxs-lookup"><span data-stu-id="03c73-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="03c73-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03c73-120">Return value</span></span>

<span data-ttu-id="03c73-121">Número</span><span class="sxs-lookup"><span data-stu-id="03c73-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="03c73-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="03c73-122">Remarks</span></span>

<span data-ttu-id="03c73-p101">El resultado tiene el mismo signo que el divisor. Se devuelve el error #DIV/0! cuando el divisor vale 0.</span><span class="sxs-lookup"><span data-stu-id="03c73-p101">The result has the same sign as the divisor. A #DIV/0! error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="03c73-126">En casi todas las ocasiones es aconsejable utilizar la función MODULUS en lugar de la función MOD.</span><span class="sxs-lookup"><span data-stu-id="03c73-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="03c73-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="03c73-127">Example 1</span></span>

<span data-ttu-id="03c73-128">MODULUS(5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="03c73-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="03c73-129">Devuelve 0,8.</span><span class="sxs-lookup"><span data-stu-id="03c73-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="03c73-130">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="03c73-130">Example 2</span></span>

<span data-ttu-id="03c73-131">MODULUS(5, -1.4)</span><span class="sxs-lookup"><span data-stu-id="03c73-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="03c73-132">Devuelve -0,6.</span><span class="sxs-lookup"><span data-stu-id="03c73-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="03c73-133">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="03c73-133">Example 3</span></span>

<span data-ttu-id="03c73-134">MODULUS(-5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="03c73-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="03c73-135">Devuelve 0,6.</span><span class="sxs-lookup"><span data-stu-id="03c73-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="03c73-136">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="03c73-136">Example 4</span></span>

<span data-ttu-id="03c73-137">MODULUS(-5, -1.4)</span><span class="sxs-lookup"><span data-stu-id="03c73-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="03c73-138">Devuelve -0,8.</span><span class="sxs-lookup"><span data-stu-id="03c73-138">Returns -0.8.</span></span>
  

