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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340127"
---
# <a name="nurbs-function"></a><span data-ttu-id="07254-104">Función NURBS</span><span class="sxs-lookup"><span data-stu-id="07254-104">NURBS Function</span></span>

<span data-ttu-id="07254-105">Devuelve una spline B racional no uniforme (NURBS).</span><span class="sxs-lookup"><span data-stu-id="07254-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="07254-106">Esta función se utiliza en la celda E de las filas de geometría NURBSto.</span><span class="sxs-lookup"><span data-stu-id="07254-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="07254-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07254-107">Syntax</span></span>

<span data-ttu-id="07254-108">NURBS (\* \* *knotLast* \* \*, \* \* *degree* \* \*, \* \* *tipoDex* \* \*, \* \* *tipoDeY* \* \*, \* \* *x1* \* \*, \* \* *Y1* \* \*, \* \* *knot1* \* \*, \* \* *Weight1* \* \*,...)</span><span class="sxs-lookup"><span data-stu-id="07254-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="07254-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07254-109">Parameters</span></span>

|<span data-ttu-id="07254-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="07254-110">**Name**</span></span>|<span data-ttu-id="07254-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="07254-111">**Required/Optional**</span></span>|<span data-ttu-id="07254-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="07254-112">**Data Type**</span></span>|<span data-ttu-id="07254-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07254-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="07254-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="07254-114">_knotLast_</span></span> <br/> |<span data-ttu-id="07254-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="07254-115">Required</span></span>  <br/> |<span data-ttu-id="07254-116">**string**</span><span class="sxs-lookup"><span data-stu-id="07254-116">**string**</span></span> <br/> | <span data-ttu-id="07254-117">El último nodo.</span><span class="sxs-lookup"><span data-stu-id="07254-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="07254-118">_grado_</span><span class="sxs-lookup"><span data-stu-id="07254-118">_degree_</span></span> <br/> |<span data-ttu-id="07254-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="07254-119">Required</span></span>  <br/> |<span data-ttu-id="07254-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="07254-120">**Numeric**</span></span> <br/> |<span data-ttu-id="07254-121">El grado de la spline.</span><span class="sxs-lookup"><span data-stu-id="07254-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="07254-122">_Alguno_</span><span class="sxs-lookup"><span data-stu-id="07254-122">_xType_</span></span> <br/> |<span data-ttu-id="07254-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="07254-123">Required</span></span>  <br/> |<span data-ttu-id="07254-124">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="07254-124">**Numeric**</span></span> <br/> |<span data-ttu-id="07254-125">Especifica cómo interpretar los datos de entrada _x_ .</span><span class="sxs-lookup"><span data-stu-id="07254-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="07254-126">Si _tipoDex_ es 0, todos los datos de entrada _x_ se interpretan como un porcentaje del ancho.</span><span class="sxs-lookup"><span data-stu-id="07254-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="07254-127">Si _tipoDex_ es 1, todos los datos de entrada _x_ se interpretan como coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="07254-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="07254-128">_tipoDeY_</span><span class="sxs-lookup"><span data-stu-id="07254-128">_yType_</span></span> <br/> |<span data-ttu-id="07254-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="07254-129">Required</span></span>  <br/> |<span data-ttu-id="07254-130">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="07254-130">**Numeric**</span></span> <br/> |<span data-ttu-id="07254-131">Especifica cómo interpretar los datos de entrada de _y_ .</span><span class="sxs-lookup"><span data-stu-id="07254-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="07254-132">Si el valor de _tipoDeY_ es 0, todos los datos de entrada de _y_ se interpretan como un porcentaje del alto.</span><span class="sxs-lookup"><span data-stu-id="07254-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="07254-133">Si _tipoDeY_ es 1, todos los datos de entrada de _y_ se interpretan como coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="07254-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="07254-134">_1_</span><span class="sxs-lookup"><span data-stu-id="07254-134">_x1_</span></span> <br/> |<span data-ttu-id="07254-135">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="07254-135">Required</span></span>  <br/> |<span data-ttu-id="07254-136">**String**</span><span class="sxs-lookup"><span data-stu-id="07254-136">**String**</span></span> <br/> |<span data-ttu-id="07254-137">Una coordenada x.</span><span class="sxs-lookup"><span data-stu-id="07254-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="07254-138">_a1_</span><span class="sxs-lookup"><span data-stu-id="07254-138">_y1_</span></span> <br/> |<span data-ttu-id="07254-139">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="07254-139">Required</span></span>  <br/> |<span data-ttu-id="07254-140">**String**</span><span class="sxs-lookup"><span data-stu-id="07254-140">**String**</span></span> <br/> |<span data-ttu-id="07254-141">Una coordenada y.</span><span class="sxs-lookup"><span data-stu-id="07254-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="07254-142">_knot1_</span><span class="sxs-lookup"><span data-stu-id="07254-142">_knot1_</span></span> <br/> |<span data-ttu-id="07254-143">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="07254-143">Required</span></span>  <br/> |<span data-ttu-id="07254-144">**String**</span><span class="sxs-lookup"><span data-stu-id="07254-144">**String**</span></span> <br/> |<span data-ttu-id="07254-145">Un nodo de la spline B.</span><span class="sxs-lookup"><span data-stu-id="07254-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="07254-146">_Weight1_</span><span class="sxs-lookup"><span data-stu-id="07254-146">_weight1_</span></span> <br/> |<span data-ttu-id="07254-147">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="07254-147">Required</span></span>  <br/> |<span data-ttu-id="07254-148">**String**</span><span class="sxs-lookup"><span data-stu-id="07254-148">**String**</span></span> <br/> |<span data-ttu-id="07254-149">Un grosor de la spline B.</span><span class="sxs-lookup"><span data-stu-id="07254-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07254-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07254-150">Remarks</span></span>

<span data-ttu-id="07254-151">Para cada argumento *x* debe haber un argumento *y* ; de lo contrario, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="07254-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="07254-152">Debe especificar al menos un argumento *x*, *y*, *nudo* y *Weight* ; de lo contrario, Visio devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="07254-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

