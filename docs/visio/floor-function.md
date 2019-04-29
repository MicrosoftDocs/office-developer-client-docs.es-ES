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
description: Redondea un número hacia el valor de 0 (cero), al siguiente entero o a la siguiente instancia de Multiple.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439901"
---
# <a name="floor-function"></a><span data-ttu-id="fdb5a-103">Función FLOOR</span><span class="sxs-lookup"><span data-stu-id="fdb5a-103">FLOOR Function</span></span>

<span data-ttu-id="fdb5a-104">Redondea un número hacia el valor de 0 (cero), al siguiente entero o a la siguiente instancia de _Multiple_.</span><span class="sxs-lookup"><span data-stu-id="fdb5a-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fdb5a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fdb5a-105">Syntax</span></span>

<span data-ttu-id="fdb5a-106">FLOOR (\* \* *número* \* \*, \* \* *varios* \* \*)</span><span class="sxs-lookup"><span data-stu-id="fdb5a-106">FLOOR(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fdb5a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdb5a-107">Parameters</span></span>

|<span data-ttu-id="fdb5a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fdb5a-108">**Name**</span></span>|<span data-ttu-id="fdb5a-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="fdb5a-109">**Required/Optional**</span></span>|<span data-ttu-id="fdb5a-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="fdb5a-110">**Data Type**</span></span>|<span data-ttu-id="fdb5a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fdb5a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fdb5a-112">_number_</span><span class="sxs-lookup"><span data-stu-id="fdb5a-112">_number_</span></span> <br/> |<span data-ttu-id="fdb5a-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fdb5a-113">Required</span></span>  <br/> |<span data-ttu-id="fdb5a-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="fdb5a-114">**Number**</span></span> <br/> |<span data-ttu-id="fdb5a-115">El número que desea redondear.</span><span class="sxs-lookup"><span data-stu-id="fdb5a-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="fdb5a-116">_distintos_</span><span class="sxs-lookup"><span data-stu-id="fdb5a-116">_multiple_</span></span> <br/> |<span data-ttu-id="fdb5a-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fdb5a-117">Required</span></span>  <br/> |<span data-ttu-id="fdb5a-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="fdb5a-118">**Number**</span></span> <br/> |<span data-ttu-id="fdb5a-119">El múltiple por el que redondear.</span><span class="sxs-lookup"><span data-stu-id="fdb5a-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fdb5a-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdb5a-120">Return value</span></span>

<span data-ttu-id="fdb5a-121">Número</span><span class="sxs-lookup"><span data-stu-id="fdb5a-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fdb5a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fdb5a-122">Remarks</span></span>

<span data-ttu-id="fdb5a-123">Si no se especifica el _múltiplo_ , el número se redondea hacia 0 hasta el siguiente entero.</span><span class="sxs-lookup"><span data-stu-id="fdb5a-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="fdb5a-124">_Número_ y _varios_ deben tener los mismos signos o un #NUM!</span><span class="sxs-lookup"><span data-stu-id="fdb5a-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="fdb5a-125">se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="fdb5a-125">error is returned.</span></span> <span data-ttu-id="fdb5a-126">Si uno o _varios_ _números_ no se pueden convertir en un valor, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="fdb5a-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="fdb5a-127">se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="fdb5a-127">error is returned.</span></span> <span data-ttu-id="fdb5a-128">Si _número_ o _múltiplo_ es 0, el resultado es 0.</span><span class="sxs-lookup"><span data-stu-id="fdb5a-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fdb5a-129">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="fdb5a-129">Example 1</span></span>

<span data-ttu-id="fdb5a-130">PISO (3.7)</span><span class="sxs-lookup"><span data-stu-id="fdb5a-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="fdb5a-131">Devuelve 3.</span><span class="sxs-lookup"><span data-stu-id="fdb5a-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fdb5a-132">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="fdb5a-132">Example 2</span></span>

<span data-ttu-id="fdb5a-133">PISO (-3,7)</span><span class="sxs-lookup"><span data-stu-id="fdb5a-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="fdb5a-134">Devuelve -3.</span><span class="sxs-lookup"><span data-stu-id="fdb5a-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fdb5a-135">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="fdb5a-135">Example 3</span></span>

<span data-ttu-id="fdb5a-136">FLOOR (3,7, 0,5)</span><span class="sxs-lookup"><span data-stu-id="fdb5a-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="fdb5a-137">Devuelve 3,5.</span><span class="sxs-lookup"><span data-stu-id="fdb5a-137">Returns 3.5.</span></span>
  

