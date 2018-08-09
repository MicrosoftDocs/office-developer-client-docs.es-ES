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
description: Redondea un número de 0 (cero) a la siguiente instancia de múltiplo. Si no se especifica múltiplo, el número se redondea dirección contraria a 0 hasta el siguiente entero.
ms.openlocfilehash: fa982b44ea4a73e7da614c49a52cd50efd612f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821709"
---
# <a name="ceiling-function"></a><span data-ttu-id="dbe7d-104">Función CEILING</span><span class="sxs-lookup"><span data-stu-id="dbe7d-104">CEILING Function</span></span>

<span data-ttu-id="dbe7d-105">Redondea un número de 0 (cero) a la siguiente aparición de _varios_.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="dbe7d-106">Si no se especifica _múltiplo_ , el número se redondea dirección contraria a 0 hasta el siguiente entero.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dbe7d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbe7d-107">Syntax</span></span>

<span data-ttu-id="dbe7d-108">CEILING (** *número* **, ** *varios* **)</span><span class="sxs-lookup"><span data-stu-id="dbe7d-108">CEILING(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dbe7d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dbe7d-109">Parameters</span></span>

|<span data-ttu-id="dbe7d-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="dbe7d-110">**Name**</span></span>|<span data-ttu-id="dbe7d-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="dbe7d-111">**Required/Optional**</span></span>|<span data-ttu-id="dbe7d-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="dbe7d-112">**Data Type**</span></span>|<span data-ttu-id="dbe7d-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dbe7d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dbe7d-114">_number_</span><span class="sxs-lookup"><span data-stu-id="dbe7d-114">_number_</span></span> <br/> |<span data-ttu-id="dbe7d-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="dbe7d-115">Required</span></span>  <br/> |<span data-ttu-id="dbe7d-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="dbe7d-116">**Number**</span></span> <br/> |<span data-ttu-id="dbe7d-117">El número que desea redondear.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="dbe7d-118">_varios_</span><span class="sxs-lookup"><span data-stu-id="dbe7d-118">_multiple_</span></span> <br/> |<span data-ttu-id="dbe7d-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="dbe7d-119">Required</span></span>  <br/> |<span data-ttu-id="dbe7d-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="dbe7d-120">**Number**</span></span> <br/> |<span data-ttu-id="dbe7d-121">Varios a redondear a.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbe7d-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dbe7d-122">Remarks</span></span>

 <span data-ttu-id="dbe7d-123">_Número_ y _varios_ deben tener el mismo signo o un #NUM!</span><span class="sxs-lookup"><span data-stu-id="dbe7d-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="dbe7d-124">se devuelve el error.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-124">error is returned.</span></span> <span data-ttu-id="dbe7d-125">Si _número_ o _múltiplo_ no se puede convertir en un valor, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="dbe7d-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="dbe7d-126">se devuelve el error.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-126">error is returned.</span></span> <span data-ttu-id="dbe7d-127">Si el _número_ o el _múltiplo_ es 0, el resultado es 0.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="dbe7d-128">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="dbe7d-128">Example 1</span></span>

<span data-ttu-id="dbe7d-129">CEILING(3.7)</span><span class="sxs-lookup"><span data-stu-id="dbe7d-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="dbe7d-130">Devuelve 4.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="dbe7d-131">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="dbe7d-131">Example 2</span></span>

<span data-ttu-id="dbe7d-132">CEILING(-3.7)</span><span class="sxs-lookup"><span data-stu-id="dbe7d-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="dbe7d-133">Devuelve -4.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="dbe7d-134">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="dbe7d-134">Example 3</span></span>

<span data-ttu-id="dbe7d-135">CEILING (3.7, 0,25)</span><span class="sxs-lookup"><span data-stu-id="dbe7d-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="dbe7d-136">Devuelve 3,75.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-136">Returns 3.75</span></span>
  

