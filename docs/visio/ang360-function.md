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
ms.openlocfilehash: 6916e50daad735843bf0a2a6361fb5b1b833e2ce
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160303"
---
# <a name="ang360-function"></a><span data-ttu-id="111c2-103">Función ANG360</span><span class="sxs-lookup"><span data-stu-id="111c2-103">ANG360 Function</span></span>

<span data-ttu-id="111c2-104">Normaliza el intervalo de un ángulo en 0 = resultado \< \< 2PI radianes (0 \< = resultado \< 360 grados).</span><span class="sxs-lookup"><span data-stu-id="111c2-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="111c2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="111c2-105">Syntax</span></span>

<span data-ttu-id="111c2-106">ANG360(***ángulo*** )</span><span class="sxs-lookup"><span data-stu-id="111c2-106">ANG360(***angle*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="111c2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="111c2-107">Parameters</span></span>

|<span data-ttu-id="111c2-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="111c2-108">**Name**</span></span>|<span data-ttu-id="111c2-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="111c2-109">**Required/Optional**</span></span>|<span data-ttu-id="111c2-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="111c2-110">**Data Type**</span></span>|<span data-ttu-id="111c2-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="111c2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="111c2-112">_ángulo_</span><span class="sxs-lookup"><span data-stu-id="111c2-112">_angle_</span></span> <br/> |<span data-ttu-id="111c2-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="111c2-113">Required</span></span>  <br/> |<span data-ttu-id="111c2-114">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="111c2-114">**Numeric**</span></span> <br/> |<span data-ttu-id="111c2-115">El ángulo que se normalizará.</span><span class="sxs-lookup"><span data-stu-id="111c2-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="111c2-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="111c2-116">Remarks</span></span>

<span data-ttu-id="111c2-117">Si  *el*  ángulo no se especifica mediante unidades angulares, se interpreta como radianes.</span><span class="sxs-lookup"><span data-stu-id="111c2-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="111c2-118">Si  *el*  ángulo no se puede convertir en un valor, #VALUE!</span><span class="sxs-lookup"><span data-stu-id="111c2-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="111c2-119">se devuelve.</span><span class="sxs-lookup"><span data-stu-id="111c2-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="111c2-120">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="111c2-120">Example 1</span></span>

<span data-ttu-id="111c2-121">ANG360(395 grad)</span><span class="sxs-lookup"><span data-stu-id="111c2-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="111c2-122">Devuelve 35 grad</span><span class="sxs-lookup"><span data-stu-id="111c2-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="111c2-123">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="111c2-123">Example 2</span></span>

<span data-ttu-id="111c2-124">ANG360(-9,8 rad)</span><span class="sxs-lookup"><span data-stu-id="111c2-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="111c2-125">Devuelve 2,7664 rad</span><span class="sxs-lookup"><span data-stu-id="111c2-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="111c2-126">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="111c2-126">Example 3</span></span>

<span data-ttu-id="111c2-127">ANG360(45)</span><span class="sxs-lookup"><span data-stu-id="111c2-127">ANG360(45)</span></span>
  
<span data-ttu-id="111c2-128">Devuelve 58,31 grad (1,0177 rad)</span><span class="sxs-lookup"><span data-stu-id="111c2-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

