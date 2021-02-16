---
title: Función DATE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Devuelve la fecha representada por el año, el mes y el día con formato de acuerdo con el estilo de fecha corta de configuración regional del sistema. Los valores de año, mes y día reflejan el calendario gregoriano.
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360336"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="68de2-104">Función DATE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="68de2-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="68de2-105">Devuelve la fecha representada por  *año, mes*  y  *día*  con formato de acuerdo con el estilo de fecha corta en la Configuración regional del sistema.</span><span class="sxs-lookup"><span data-stu-id="68de2-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="68de2-106">Los valores de  *año,* *mes*  y  *día*  reflejan el calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="68de2-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="68de2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68de2-107">Syntax</span></span>

<span data-ttu-id="68de2-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span><span class="sxs-lookup"><span data-stu-id="68de2-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="68de2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68de2-109">Parameters</span></span>

|<span data-ttu-id="68de2-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="68de2-110">**Name**</span></span>|<span data-ttu-id="68de2-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="68de2-111">**Required/Optional**</span></span>|<span data-ttu-id="68de2-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="68de2-112">**Data Type**</span></span>|<span data-ttu-id="68de2-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="68de2-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="68de2-114">_year_</span><span class="sxs-lookup"><span data-stu-id="68de2-114">_year_</span></span> <br/> |<span data-ttu-id="68de2-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="68de2-115">Required</span></span>  <br/> |<span data-ttu-id="68de2-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="68de2-116">**Integer**</span></span> <br/> |<span data-ttu-id="68de2-117">El año.</span><span class="sxs-lookup"><span data-stu-id="68de2-117">The year.</span></span>  <br/> |
| <span data-ttu-id="68de2-118">_month_</span><span class="sxs-lookup"><span data-stu-id="68de2-118">_month_</span></span> <br/> |<span data-ttu-id="68de2-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="68de2-119">Required</span></span>  <br/> |<span data-ttu-id="68de2-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="68de2-120">**Integer**</span></span> <br/> |<span data-ttu-id="68de2-121">El mes.</span><span class="sxs-lookup"><span data-stu-id="68de2-121">The month.</span></span>  <br/> |
| <span data-ttu-id="68de2-122">_day_</span><span class="sxs-lookup"><span data-stu-id="68de2-122">_day_</span></span> <br/> |<span data-ttu-id="68de2-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="68de2-123">Required</span></span>  <br/> |<span data-ttu-id="68de2-124">**Integer**</span><span class="sxs-lookup"><span data-stu-id="68de2-124">**Integer**</span></span> <br/> |<span data-ttu-id="68de2-125">El día.</span><span class="sxs-lookup"><span data-stu-id="68de2-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="68de2-126">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="68de2-126">Example 1</span></span>

<span data-ttu-id="68de2-127">DATE(1999,6,7)</span><span class="sxs-lookup"><span data-stu-id="68de2-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="68de2-128">Devuelve el valor que corresponde al 07/06/99.</span><span class="sxs-lookup"><span data-stu-id="68de2-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="68de2-129">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="68de2-129">Example 2</span></span>

<span data-ttu-id="68de2-130">DATE(1999;6;7) + 4 ed.</span><span class="sxs-lookup"><span data-stu-id="68de2-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="68de2-131">Devuelve el valor que corresponde al 11/06/99.</span><span class="sxs-lookup"><span data-stu-id="68de2-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="68de2-132">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="68de2-132">Example 3</span></span>

<span data-ttu-id="68de2-133">FORMAT(DATE(1999,10,14),"C")</span><span class="sxs-lookup"><span data-stu-id="68de2-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="68de2-134">Devuelve el valor que corresponde al 14/10/99.</span><span class="sxs-lookup"><span data-stu-id="68de2-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

