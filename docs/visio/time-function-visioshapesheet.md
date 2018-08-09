---
title: TIME Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Devuelve la hora representada por hora, minuto y segundo.
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823421"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="ba1ce-103">TIME Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="ba1ce-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="ba1ce-104">Devuelve la hora representada por _hora_, _minuto_y _segundo_.</span><span class="sxs-lookup"><span data-stu-id="ba1ce-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ba1ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba1ce-105">Syntax</span></span>

<span data-ttu-id="ba1ce-106">TIEMPO (** *hora* **, ** *minuto* **, ** *segundo* **)</span><span class="sxs-lookup"><span data-stu-id="ba1ce-106">TIME(** *hour* **, ** *minute* **, ** *second* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ba1ce-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba1ce-107">Parameters</span></span>

|<span data-ttu-id="ba1ce-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ba1ce-108">**Name**</span></span>|<span data-ttu-id="ba1ce-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="ba1ce-109">**Required/Optional**</span></span>|<span data-ttu-id="ba1ce-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ba1ce-110">**Data Type**</span></span>|<span data-ttu-id="ba1ce-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba1ce-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ba1ce-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="ba1ce-112">_hour_</span></span> <br/> |<span data-ttu-id="ba1ce-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ba1ce-113">Required</span></span>  <br/> |<span data-ttu-id="ba1ce-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ba1ce-114">**Numeric**</span></span> <br/> |<span data-ttu-id="ba1ce-115">El componente de hora.</span><span class="sxs-lookup"><span data-stu-id="ba1ce-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="ba1ce-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="ba1ce-116">_minute_</span></span> <br/> |<span data-ttu-id="ba1ce-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ba1ce-117">Required</span></span>  <br/> |<span data-ttu-id="ba1ce-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ba1ce-118">**Numeric**</span></span> <br/> |<span data-ttu-id="ba1ce-119">El componente de minuto.</span><span class="sxs-lookup"><span data-stu-id="ba1ce-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="ba1ce-120">_second_</span><span class="sxs-lookup"><span data-stu-id="ba1ce-120">_second_</span></span> <br/> |<span data-ttu-id="ba1ce-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ba1ce-121">Required</span></span>  <br/> |<span data-ttu-id="ba1ce-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ba1ce-122">**Numeric**</span></span> <br/> |<span data-ttu-id="ba1ce-123">El componente de segundo.</span><span class="sxs-lookup"><span data-stu-id="ba1ce-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ba1ce-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba1ce-124">Return value</span></span>

<span data-ttu-id="ba1ce-125">Numeric</span><span class="sxs-lookup"><span data-stu-id="ba1ce-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="ba1ce-126">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ba1ce-126">Example 1</span></span>

<span data-ttu-id="ba1ce-127">TIME(15,30,30)</span><span class="sxs-lookup"><span data-stu-id="ba1ce-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="ba1ce-128">Devuelve el valor que representa las 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="ba1ce-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ba1ce-129">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ba1ce-129">Example 2</span></span>

<span data-ttu-id="ba1ce-130">FORMAT(TIME(15,30,30),"HH:mm")</span><span class="sxs-lookup"><span data-stu-id="ba1ce-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="ba1ce-131">Devuelve el valor que representa las 15:30.</span><span class="sxs-lookup"><span data-stu-id="ba1ce-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ba1ce-132">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="ba1ce-132">Example 3</span></span>

<span data-ttu-id="ba1ce-133">TIME(15,30,30) + 8 eh.</span><span class="sxs-lookup"><span data-stu-id="ba1ce-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="ba1ce-134">Devuelve el valor que representa las 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="ba1ce-134">Returns the value representing 23:30:30.</span></span>
  

