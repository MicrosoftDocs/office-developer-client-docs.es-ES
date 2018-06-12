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
description: Devuelve el resto (módulo) que se produce cuando se divide un número por un divisor.
ms.openlocfilehash: 4e2ef7acf9dc04e788cb2b8a0ff737f12a79c61a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822661"
---
# <a name="modulus-function"></a><span data-ttu-id="16b38-103">MODULUS (función)</span><span class="sxs-lookup"><span data-stu-id="16b38-103">MODULUS Function</span></span>

<span data-ttu-id="16b38-104">Devuelve el resto (módulo) que se produce cuando se divide un número por un divisor.</span><span class="sxs-lookup"><span data-stu-id="16b38-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="16b38-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16b38-105">Syntax</span></span>

<span data-ttu-id="16b38-106">MODULUS (** *número* **, ** *divisor* **)</span><span class="sxs-lookup"><span data-stu-id="16b38-106">MODULUS(** *number* **, ** *divisor* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="16b38-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16b38-107">Parameters</span></span>

|<span data-ttu-id="16b38-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="16b38-108">**Name**</span></span>|<span data-ttu-id="16b38-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="16b38-109">**Required/Optional**</span></span>|<span data-ttu-id="16b38-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="16b38-110">**Data Type**</span></span>|<span data-ttu-id="16b38-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16b38-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="16b38-112">_number_</span><span class="sxs-lookup"><span data-stu-id="16b38-112">_number_</span></span> <br/> |<span data-ttu-id="16b38-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="16b38-113">Required</span></span>  <br/> |<span data-ttu-id="16b38-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="16b38-114">**Number**</span></span> <br/> |<span data-ttu-id="16b38-115">El dividendo.</span><span class="sxs-lookup"><span data-stu-id="16b38-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="16b38-116">_divisor_</span><span class="sxs-lookup"><span data-stu-id="16b38-116">_divisor_</span></span> <br/> |<span data-ttu-id="16b38-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="16b38-117">Required</span></span>  <br/> |<span data-ttu-id="16b38-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="16b38-118">**Number**</span></span> <br/> |<span data-ttu-id="16b38-119">El divisor.</span><span class="sxs-lookup"><span data-stu-id="16b38-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="16b38-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16b38-120">Return value</span></span>

<span data-ttu-id="16b38-121">Number</span><span class="sxs-lookup"><span data-stu-id="16b38-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16b38-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16b38-122">Remarks</span></span>

<span data-ttu-id="16b38-p101">El resultado tiene el mismo signo que el divisor. Se devuelve el error #DIV/0! cuando el divisor vale 0.</span><span class="sxs-lookup"><span data-stu-id="16b38-p101">The result has the same sign as the divisor. A #DIV/0! error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="16b38-126">En casi todas las ocasiones es aconsejable utilizar la función MODULUS en lugar de la función MOD.</span><span class="sxs-lookup"><span data-stu-id="16b38-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="16b38-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="16b38-127">Example 1</span></span>

<span data-ttu-id="16b38-128">MODULUS(5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="16b38-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="16b38-129">Devuelve 0,8.</span><span class="sxs-lookup"><span data-stu-id="16b38-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="16b38-130">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="16b38-130">Example 2</span></span>

<span data-ttu-id="16b38-131">MODULUS(5, -1.4)</span><span class="sxs-lookup"><span data-stu-id="16b38-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="16b38-132">Devuelve -0,6.</span><span class="sxs-lookup"><span data-stu-id="16b38-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="16b38-133">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="16b38-133">Example 3</span></span>

<span data-ttu-id="16b38-134">MODULUS(-5, 1,4)</span><span class="sxs-lookup"><span data-stu-id="16b38-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="16b38-135">Devuelve 0,6.</span><span class="sxs-lookup"><span data-stu-id="16b38-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="16b38-136">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="16b38-136">Example 4</span></span>

<span data-ttu-id="16b38-137">MODULUS(-5, -1.4)</span><span class="sxs-lookup"><span data-stu-id="16b38-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="16b38-138">Devuelve -0,8.</span><span class="sxs-lookup"><span data-stu-id="16b38-138">Returns -0.8.</span></span>
  

