---
title: ANG360 (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Normaliza el intervalo de un ángulo.
ms.openlocfilehash: 01092e06b55c73953417fe7d0fa1c9f74d668922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821521"
---
# <a name="ang360-function"></a><span data-ttu-id="b880e-103">ANG360 (función)</span><span class="sxs-lookup"><span data-stu-id="b880e-103">ANG360 Function</span></span>

<span data-ttu-id="b880e-104">Normaliza el intervalo de un ángulo para que sea 0 \<= resultado \< 2 pi radianes (0 \<= resultado \< 360 grados).</span><span class="sxs-lookup"><span data-stu-id="b880e-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b880e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b880e-105">Syntax</span></span>

<span data-ttu-id="b880e-106">ANG360 (** *ángulo* **)</span><span class="sxs-lookup"><span data-stu-id="b880e-106">ANG360(** *angle* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b880e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b880e-107">Parameters</span></span>

|<span data-ttu-id="b880e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b880e-108">**Name**</span></span>|<span data-ttu-id="b880e-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="b880e-109">**Required/Optional**</span></span>|<span data-ttu-id="b880e-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="b880e-110">**Data Type**</span></span>|<span data-ttu-id="b880e-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b880e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b880e-112">_ángulo_</span><span class="sxs-lookup"><span data-stu-id="b880e-112">_angle_</span></span> <br/> |<span data-ttu-id="b880e-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b880e-113">Required</span></span>  <br/> |<span data-ttu-id="b880e-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="b880e-114">**Numeric**</span></span> <br/> |<span data-ttu-id="b880e-115">El ángulo que se normalizará.</span><span class="sxs-lookup"><span data-stu-id="b880e-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b880e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b880e-116">Remarks</span></span>

<span data-ttu-id="b880e-117">Si no se especifica el *ángulo* mediante el uso de unidades angulares, se interpreta como radianes.</span><span class="sxs-lookup"><span data-stu-id="b880e-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="b880e-118">Si el *ángulo* no se puede convertir en un valor, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="b880e-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="b880e-119">se devuelve el error.</span><span class="sxs-lookup"><span data-stu-id="b880e-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="b880e-120">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="b880e-120">Example 1</span></span>

<span data-ttu-id="b880e-121">ANG360(395 grad)</span><span class="sxs-lookup"><span data-stu-id="b880e-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="b880e-122">Devuelve 35 grad</span><span class="sxs-lookup"><span data-stu-id="b880e-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b880e-123">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="b880e-123">Example 2</span></span>

<span data-ttu-id="b880e-124">ANG360(-9,8 rad)</span><span class="sxs-lookup"><span data-stu-id="b880e-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="b880e-125">Devuelve 2,7664 rad</span><span class="sxs-lookup"><span data-stu-id="b880e-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b880e-126">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="b880e-126">Example 3</span></span>

<span data-ttu-id="b880e-127">ANG360(45)</span><span class="sxs-lookup"><span data-stu-id="b880e-127">ANG360(45)</span></span>
  
<span data-ttu-id="b880e-128">Devuelve 58,31 grad (1,0177 rad)</span><span class="sxs-lookup"><span data-stu-id="b880e-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

