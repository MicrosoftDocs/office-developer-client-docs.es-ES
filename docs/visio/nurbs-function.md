---
title: NURBS (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Devuelve una B-spline racional no uniforme (NURBS). Esta función se usa en la celda E de las filas de geometría NURBSTo.
ms.openlocfilehash: 005a66b9da2425beaf416ec2273c10446c183add
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822719"
---
# <a name="nurbs-function"></a><span data-ttu-id="5c5b2-104">NURBS (función)</span><span class="sxs-lookup"><span data-stu-id="5c5b2-104">NURBS Function</span></span>

<span data-ttu-id="5c5b2-105">Devuelve una B-spline racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="5c5b2-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="5c5b2-106">Esta función se usa en la celda E de las filas de geometría NURBSTo.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5c5b2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c5b2-107">Syntax</span></span>

<span data-ttu-id="5c5b2-108">NURBS (** *últimoPunto* **, ** *grado* **, ** *tipoDeX* **, ** *tipoDeY* **, ** *x1* **, ** *y1* **, ** *punto1* **, ** *grosor1* **, …)</span><span class="sxs-lookup"><span data-stu-id="5c5b2-108">NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5c5b2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c5b2-109">Parameters</span></span>

|<span data-ttu-id="5c5b2-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-110">**Name**</span></span>|<span data-ttu-id="5c5b2-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-111">**Required/Optional**</span></span>|<span data-ttu-id="5c5b2-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-112">**Data Type**</span></span>|<span data-ttu-id="5c5b2-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5c5b2-114">_últimoPunto_</span><span class="sxs-lookup"><span data-stu-id="5c5b2-114">_knotLast_</span></span> <br/> |<span data-ttu-id="5c5b2-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c5b2-115">Required</span></span>  <br/> |<span data-ttu-id="5c5b2-116">**string**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-116">**string**</span></span> <br/> | <span data-ttu-id="5c5b2-117">El último nodo.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="5c5b2-118">_grado_</span><span class="sxs-lookup"><span data-stu-id="5c5b2-118">_degree_</span></span> <br/> |<span data-ttu-id="5c5b2-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c5b2-119">Required</span></span>  <br/> |<span data-ttu-id="5c5b2-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-120">**Numeric**</span></span> <br/> |<span data-ttu-id="5c5b2-121">El grado de la spline.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="5c5b2-122">_tipoDeX_</span><span class="sxs-lookup"><span data-stu-id="5c5b2-122">_xType_</span></span> <br/> |<span data-ttu-id="5c5b2-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c5b2-123">Required</span></span>  <br/> |<span data-ttu-id="5c5b2-124">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-124">**Numeric**</span></span> <br/> |<span data-ttu-id="5c5b2-125">Especifica cómo interpretar los datos de entrada de _x_ .</span><span class="sxs-lookup"><span data-stu-id="5c5b2-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="5c5b2-126">Si el _valor de tipoDeX_ es 0, todos los datos de entrada de _x_ se interpreta como un porcentaje del ancho.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="5c5b2-127">Si _es 1,_ todos los datos de entrada de _x_ se interpreta como coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="5c5b2-128">_dos valores_</span><span class="sxs-lookup"><span data-stu-id="5c5b2-128">_yType_</span></span> <br/> |<span data-ttu-id="5c5b2-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c5b2-129">Required</span></span>  <br/> |<span data-ttu-id="5c5b2-130">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-130">**Numeric**</span></span> <br/> |<span data-ttu-id="5c5b2-131">Especifica cómo interpretar los datos de entrada de _y_ .</span><span class="sxs-lookup"><span data-stu-id="5c5b2-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="5c5b2-132">Si _es 0,_ todos los datos de entrada _y_ se interpreta como un porcentaje del alto.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="5c5b2-133">Si _es 1,_ todos los datos de entrada de _y_ se interpretan como coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="5c5b2-134">_X1_</span><span class="sxs-lookup"><span data-stu-id="5c5b2-134">_x1_</span></span> <br/> |<span data-ttu-id="5c5b2-135">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c5b2-135">Required</span></span>  <br/> |<span data-ttu-id="5c5b2-136">**String**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-136">**String**</span></span> <br/> |<span data-ttu-id="5c5b2-137">Una coordenada x.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="5c5b2-138">_Y1_</span><span class="sxs-lookup"><span data-stu-id="5c5b2-138">_y1_</span></span> <br/> |<span data-ttu-id="5c5b2-139">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c5b2-139">Required</span></span>  <br/> |<span data-ttu-id="5c5b2-140">**String**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-140">**String**</span></span> <br/> |<span data-ttu-id="5c5b2-141">Una coordenada y.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="5c5b2-142">_punto1_</span><span class="sxs-lookup"><span data-stu-id="5c5b2-142">_knot1_</span></span> <br/> |<span data-ttu-id="5c5b2-143">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c5b2-143">Required</span></span>  <br/> |<span data-ttu-id="5c5b2-144">**String**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-144">**String**</span></span> <br/> |<span data-ttu-id="5c5b2-145">Un nodo de la spline B.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="5c5b2-146">_grosor1_</span><span class="sxs-lookup"><span data-stu-id="5c5b2-146">_weight1_</span></span> <br/> |<span data-ttu-id="5c5b2-147">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5c5b2-147">Required</span></span>  <br/> |<span data-ttu-id="5c5b2-148">**String**</span><span class="sxs-lookup"><span data-stu-id="5c5b2-148">**String**</span></span> <br/> |<span data-ttu-id="5c5b2-149">Un grosor de la spline B.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c5b2-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c5b2-150">Remarks</span></span>

<span data-ttu-id="5c5b2-151">Para cada argumento *x* debe haber un argumento *y* ; de lo contrario, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="5c5b2-152">Debe especificar al menos una *x*, *y*, *nodo* y argumento de *peso* ; de lo contrario, Visio devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="5c5b2-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

