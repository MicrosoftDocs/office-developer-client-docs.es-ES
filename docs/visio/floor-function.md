---
title: FLOOR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Redondea un número hacia 0 (cero), al siguiente valor entero o a la siguiente instancia de múltiplo.
ms.openlocfilehash: f66b993e3ab48fd1abc685b7db5889d5bf24fbfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822151"
---
# <a name="floor-function"></a><span data-ttu-id="5fcd4-103">Función FLOOR</span><span class="sxs-lookup"><span data-stu-id="5fcd4-103">FLOOR Function</span></span>

<span data-ttu-id="5fcd4-104">Redondea un número hacia 0 (cero), hasta el siguiente entero o hasta la siguiente instancia de _múltiplo_.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5fcd4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5fcd4-105">Syntax</span></span>

<span data-ttu-id="5fcd4-106">FLOOR (** *número* **, ** *varios* **)</span><span class="sxs-lookup"><span data-stu-id="5fcd4-106">FLOOR(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5fcd4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5fcd4-107">Parameters</span></span>

|<span data-ttu-id="5fcd4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5fcd4-108">**Name**</span></span>|<span data-ttu-id="5fcd4-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="5fcd4-109">**Required/Optional**</span></span>|<span data-ttu-id="5fcd4-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5fcd4-110">**Data Type**</span></span>|<span data-ttu-id="5fcd4-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5fcd4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5fcd4-112">_number_</span><span class="sxs-lookup"><span data-stu-id="5fcd4-112">_number_</span></span> <br/> |<span data-ttu-id="5fcd4-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5fcd4-113">Required</span></span>  <br/> |<span data-ttu-id="5fcd4-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="5fcd4-114">**Number**</span></span> <br/> |<span data-ttu-id="5fcd4-115">El número que desea redondear.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="5fcd4-116">_varios_</span><span class="sxs-lookup"><span data-stu-id="5fcd4-116">_multiple_</span></span> <br/> |<span data-ttu-id="5fcd4-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5fcd4-117">Required</span></span>  <br/> |<span data-ttu-id="5fcd4-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="5fcd4-118">**Number**</span></span> <br/> |<span data-ttu-id="5fcd4-119">El múltiple por el que redondear.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5fcd4-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5fcd4-120">Return value</span></span>

<span data-ttu-id="5fcd4-121">Number</span><span class="sxs-lookup"><span data-stu-id="5fcd4-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fcd4-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5fcd4-122">Remarks</span></span>

<span data-ttu-id="5fcd4-123">Si no se especifica _múltiplo_ , el número se redondea hacia 0 hasta el siguiente entero.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="5fcd4-124">_Número_ y _varios_ deben tener el mismo signo o un #NUM!</span><span class="sxs-lookup"><span data-stu-id="5fcd4-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="5fcd4-125">se devuelve el error.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-125">error is returned.</span></span> <span data-ttu-id="5fcd4-126">Si _número_ o _múltiplo_ no se puede convertir en un valor, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="5fcd4-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="5fcd4-127">se devuelve el error.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-127">error is returned.</span></span> <span data-ttu-id="5fcd4-128">Si el _número_ o el _múltiplo_ es 0, el resultado es 0.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="5fcd4-129">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="5fcd4-129">Example 1</span></span>

<span data-ttu-id="5fcd4-130">FLOOR(3.7)</span><span class="sxs-lookup"><span data-stu-id="5fcd4-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="5fcd4-131">Devuelve 3.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5fcd4-132">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="5fcd4-132">Example 2</span></span>

<span data-ttu-id="5fcd4-133">FLOOR(-3.7)</span><span class="sxs-lookup"><span data-stu-id="5fcd4-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="5fcd4-134">Devuelve -3.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="5fcd4-135">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="5fcd4-135">Example 3</span></span>

<span data-ttu-id="5fcd4-136">FLOOR (3.7, 0,5)</span><span class="sxs-lookup"><span data-stu-id="5fcd4-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="5fcd4-137">Devuelve 3,5.</span><span class="sxs-lookup"><span data-stu-id="5fcd4-137">Returns 3.5.</span></span>
  

