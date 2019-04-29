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
description: Devuelve una spline B racional no uniforme (NURBS). Esta función se utiliza en la celda E de las filas de geometría NURBSto.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438459"
---
# <a name="nurbs-function"></a><span data-ttu-id="d83df-104">Función NURBS</span><span class="sxs-lookup"><span data-stu-id="d83df-104">NURBS Function</span></span>

<span data-ttu-id="d83df-105">Devuelve una spline B racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="d83df-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="d83df-106">Esta función se utiliza en la celda E de las filas de geometría NURBSto.</span><span class="sxs-lookup"><span data-stu-id="d83df-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d83df-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d83df-107">Syntax</span></span>

<span data-ttu-id="d83df-108">NURBS (\* \* *knotLast* \* \*, \* \* *degree* \* \*, \* \* *tipoDex* \* \*, \* \* *tipoDeY* \* \*, \* \* *x1* \* \*, \* \* *Y1* \* \*, \* \* *knot1* \* \*, \* \* *Weight1* \* \*,...)</span><span class="sxs-lookup"><span data-stu-id="d83df-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d83df-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d83df-109">Parameters</span></span>

|<span data-ttu-id="d83df-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="d83df-110">**Name**</span></span>|<span data-ttu-id="d83df-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="d83df-111">**Required/Optional**</span></span>|<span data-ttu-id="d83df-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="d83df-112">**Data Type**</span></span>|<span data-ttu-id="d83df-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d83df-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d83df-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="d83df-114">_knotLast_</span></span> <br/> |<span data-ttu-id="d83df-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d83df-115">Required</span></span>  <br/> |<span data-ttu-id="d83df-116">**string**</span><span class="sxs-lookup"><span data-stu-id="d83df-116">**string**</span></span> <br/> | <span data-ttu-id="d83df-117">El último nodo.</span><span class="sxs-lookup"><span data-stu-id="d83df-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="d83df-118">_grado_</span><span class="sxs-lookup"><span data-stu-id="d83df-118">_degree_</span></span> <br/> |<span data-ttu-id="d83df-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d83df-119">Required</span></span>  <br/> |<span data-ttu-id="d83df-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="d83df-120">**Numeric**</span></span> <br/> |<span data-ttu-id="d83df-121">El grado de la spline.</span><span class="sxs-lookup"><span data-stu-id="d83df-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="d83df-122">_Alguno_</span><span class="sxs-lookup"><span data-stu-id="d83df-122">_xType_</span></span> <br/> |<span data-ttu-id="d83df-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d83df-123">Required</span></span>  <br/> |<span data-ttu-id="d83df-124">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="d83df-124">**Numeric**</span></span> <br/> |<span data-ttu-id="d83df-125">Especifica cómo interpretar los datos de entrada _x_ .</span><span class="sxs-lookup"><span data-stu-id="d83df-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="d83df-126">Si _tipoDex_ es 0, todos los datos de entrada _x_ se interpretan como un porcentaje del ancho.</span><span class="sxs-lookup"><span data-stu-id="d83df-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="d83df-127">Si _tipoDex_ es 1, todos los datos de entrada _x_ se interpretan como coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="d83df-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="d83df-128">_tipoDeY_</span><span class="sxs-lookup"><span data-stu-id="d83df-128">_yType_</span></span> <br/> |<span data-ttu-id="d83df-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d83df-129">Required</span></span>  <br/> |<span data-ttu-id="d83df-130">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="d83df-130">**Numeric**</span></span> <br/> |<span data-ttu-id="d83df-131">Especifica cómo interpretar los datos de entrada de _y_ .</span><span class="sxs-lookup"><span data-stu-id="d83df-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="d83df-132">Si el valor de _tipoDeY_ es 0, todos los datos de entrada de _y_ se interpretan como un porcentaje del alto.</span><span class="sxs-lookup"><span data-stu-id="d83df-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="d83df-133">Si _tipoDeY_ es 1, todos los datos de entrada de _y_ se interpretan como coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="d83df-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="d83df-134">_1_</span><span class="sxs-lookup"><span data-stu-id="d83df-134">_x1_</span></span> <br/> |<span data-ttu-id="d83df-135">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d83df-135">Required</span></span>  <br/> |<span data-ttu-id="d83df-136">**String**</span><span class="sxs-lookup"><span data-stu-id="d83df-136">**String**</span></span> <br/> |<span data-ttu-id="d83df-137">Una coordenada x.</span><span class="sxs-lookup"><span data-stu-id="d83df-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="d83df-138">_a1_</span><span class="sxs-lookup"><span data-stu-id="d83df-138">_y1_</span></span> <br/> |<span data-ttu-id="d83df-139">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d83df-139">Required</span></span>  <br/> |<span data-ttu-id="d83df-140">**String**</span><span class="sxs-lookup"><span data-stu-id="d83df-140">**String**</span></span> <br/> |<span data-ttu-id="d83df-141">Una coordenada y.</span><span class="sxs-lookup"><span data-stu-id="d83df-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="d83df-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="d83df-142">_knot1_</span></span> <br/> |<span data-ttu-id="d83df-143">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d83df-143">Required</span></span>  <br/> |<span data-ttu-id="d83df-144">**String**</span><span class="sxs-lookup"><span data-stu-id="d83df-144">**String**</span></span> <br/> |<span data-ttu-id="d83df-145">Un nodo de la spline B.</span><span class="sxs-lookup"><span data-stu-id="d83df-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="d83df-146">_Weight1_</span><span class="sxs-lookup"><span data-stu-id="d83df-146">_weight1_</span></span> <br/> |<span data-ttu-id="d83df-147">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d83df-147">Required</span></span>  <br/> |<span data-ttu-id="d83df-148">**String**</span><span class="sxs-lookup"><span data-stu-id="d83df-148">**String**</span></span> <br/> |<span data-ttu-id="d83df-149">Un grosor de la spline B.</span><span class="sxs-lookup"><span data-stu-id="d83df-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d83df-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d83df-150">Remarks</span></span>

<span data-ttu-id="d83df-151">Para cada argumento *x* debe haber un argumento *y* ; de lo contrario, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="d83df-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="d83df-152">Debe especificar al menos un argumento *x*, *y*, *nudo* y *Weight* ; de lo contrario, Visio devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="d83df-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

