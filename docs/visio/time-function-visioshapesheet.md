---
title: Función TIME (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Devuelve la hora representada por hora, minuto y segundo.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281000"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="09c1e-103">Función TIME (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="09c1e-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="09c1e-104">Devuelve la hora representada por _hora_, _minuto_y _segundo_.</span><span class="sxs-lookup"><span data-stu-id="09c1e-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="09c1e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09c1e-105">Syntax</span></span>

<span data-ttu-id="09c1e-106">TIEMPO (\* \* *hora* \* \*, \* \* *minuto* \* \*, \* \* *segundo* \* \*)</span><span class="sxs-lookup"><span data-stu-id="09c1e-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="09c1e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09c1e-107">Parameters</span></span>

|<span data-ttu-id="09c1e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="09c1e-108">**Name**</span></span>|<span data-ttu-id="09c1e-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="09c1e-109">**Required/Optional**</span></span>|<span data-ttu-id="09c1e-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="09c1e-110">**Data Type**</span></span>|<span data-ttu-id="09c1e-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="09c1e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="09c1e-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="09c1e-112">_hour_</span></span> <br/> |<span data-ttu-id="09c1e-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="09c1e-113">Required</span></span>  <br/> |<span data-ttu-id="09c1e-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="09c1e-114">**Numeric**</span></span> <br/> |<span data-ttu-id="09c1e-115">El componente de hora.</span><span class="sxs-lookup"><span data-stu-id="09c1e-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="09c1e-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="09c1e-116">_minute_</span></span> <br/> |<span data-ttu-id="09c1e-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="09c1e-117">Required</span></span>  <br/> |<span data-ttu-id="09c1e-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="09c1e-118">**Numeric**</span></span> <br/> |<span data-ttu-id="09c1e-119">El componente de minuto.</span><span class="sxs-lookup"><span data-stu-id="09c1e-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="09c1e-120">_second_</span><span class="sxs-lookup"><span data-stu-id="09c1e-120">_second_</span></span> <br/> |<span data-ttu-id="09c1e-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="09c1e-121">Required</span></span>  <br/> |<span data-ttu-id="09c1e-122">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="09c1e-122">**Numeric**</span></span> <br/> |<span data-ttu-id="09c1e-123">El componente de segundo.</span><span class="sxs-lookup"><span data-stu-id="09c1e-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="09c1e-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09c1e-124">Return value</span></span>

<span data-ttu-id="09c1e-125">Numeric</span><span class="sxs-lookup"><span data-stu-id="09c1e-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="09c1e-126">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="09c1e-126">Example 1</span></span>

<span data-ttu-id="09c1e-127">HORA (15, 30, 30)</span><span class="sxs-lookup"><span data-stu-id="09c1e-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="09c1e-128">Devuelve el valor que representa las 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="09c1e-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="09c1e-129">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="09c1e-129">Example 2</span></span>

<span data-ttu-id="09c1e-130">FORMAT (tiempo (15, 30, 30), "HH: mm")</span><span class="sxs-lookup"><span data-stu-id="09c1e-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="09c1e-131">Devuelve el valor que representa las 15:30.</span><span class="sxs-lookup"><span data-stu-id="09c1e-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="09c1e-132">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="09c1e-132">Example 3</span></span>

<span data-ttu-id="09c1e-133">TIME(15,30,30) + 8 eh.</span><span class="sxs-lookup"><span data-stu-id="09c1e-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="09c1e-134">Devuelve el valor que representa las 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="09c1e-134">Returns the value representing 23:30:30.</span></span>
  

