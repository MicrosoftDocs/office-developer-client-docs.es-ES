---
title: DATE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Devuelve la fecha representada por año, mes y día con el formato corresponde al estilo corto de fecha en la configuración Regional del sistema. Los valores de año, mes y día reflejan el calendario gregoriano.
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821943"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="8f91e-104">DATE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="8f91e-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="8f91e-105">Devuelve la fecha representada por *año, mes* y *día* con el formato corresponde al estilo corto de fecha en la configuración Regional del sistema.</span><span class="sxs-lookup"><span data-stu-id="8f91e-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="8f91e-106">Los valores de *año*, *mes* y *día* reflejan el calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="8f91e-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8f91e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f91e-107">Syntax</span></span>

<span data-ttu-id="8f91e-108">FECHA (** *año* **, ** *mes* **, ** *día* **)</span><span class="sxs-lookup"><span data-stu-id="8f91e-108">DATE(** *year* **, ** *month* **, ** *day* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8f91e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f91e-109">Parameters</span></span>

|<span data-ttu-id="8f91e-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8f91e-110">**Name**</span></span>|<span data-ttu-id="8f91e-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="8f91e-111">**Required/Optional**</span></span>|<span data-ttu-id="8f91e-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="8f91e-112">**Data Type**</span></span>|<span data-ttu-id="8f91e-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f91e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8f91e-114">_year_</span><span class="sxs-lookup"><span data-stu-id="8f91e-114">_year_</span></span> <br/> |<span data-ttu-id="8f91e-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8f91e-115">Required</span></span>  <br/> |<span data-ttu-id="8f91e-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8f91e-116">**Integer**</span></span> <br/> |<span data-ttu-id="8f91e-117">El año.</span><span class="sxs-lookup"><span data-stu-id="8f91e-117">The year.</span></span>  <br/> |
| <span data-ttu-id="8f91e-118">_month_</span><span class="sxs-lookup"><span data-stu-id="8f91e-118">_month_</span></span> <br/> |<span data-ttu-id="8f91e-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8f91e-119">Required</span></span>  <br/> |<span data-ttu-id="8f91e-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8f91e-120">**Integer**</span></span> <br/> |<span data-ttu-id="8f91e-121">El mes.</span><span class="sxs-lookup"><span data-stu-id="8f91e-121">The month.</span></span>  <br/> |
| <span data-ttu-id="8f91e-122">_day_</span><span class="sxs-lookup"><span data-stu-id="8f91e-122">_day_</span></span> <br/> |<span data-ttu-id="8f91e-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8f91e-123">Required</span></span>  <br/> |<span data-ttu-id="8f91e-124">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8f91e-124">**Integer**</span></span> <br/> |<span data-ttu-id="8f91e-125">El día.</span><span class="sxs-lookup"><span data-stu-id="8f91e-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="8f91e-126">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f91e-126">Example 1</span></span>

<span data-ttu-id="8f91e-127">DATE(1999;6;7)</span><span class="sxs-lookup"><span data-stu-id="8f91e-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="8f91e-128">Devuelve el valor que corresponde al 07/06/99.</span><span class="sxs-lookup"><span data-stu-id="8f91e-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8f91e-129">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="8f91e-129">Example 2</span></span>

<span data-ttu-id="8f91e-130">DATE(1999;6;7) + 4 ed.</span><span class="sxs-lookup"><span data-stu-id="8f91e-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="8f91e-131">Devuelve el valor que corresponde al 11/06/99.</span><span class="sxs-lookup"><span data-stu-id="8f91e-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="8f91e-132">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="8f91e-132">Example 3</span></span>

<span data-ttu-id="8f91e-133">FORMAT(DATE(1999,10,14),"C")</span><span class="sxs-lookup"><span data-stu-id="8f91e-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="8f91e-134">Devuelve el valor que corresponde al 14/10/99.</span><span class="sxs-lookup"><span data-stu-id="8f91e-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

