---
title: POLYLINE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Devuelve una polilínea. Esta función se usa en la celda A de las filas de geometría poliLíneas.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348282"
---
# <a name="polyline-function"></a><span data-ttu-id="a835c-104">Función POLYLINE</span><span class="sxs-lookup"><span data-stu-id="a835c-104">POLYLINE Function</span></span>

<span data-ttu-id="a835c-105">Devuelve una polilínea.</span><span class="sxs-lookup"><span data-stu-id="a835c-105">Returns a polyline.</span></span> <span data-ttu-id="a835c-106">Esta función se usa en la celda A de las filas de geometría poliLíneas.</span><span class="sxs-lookup"><span data-stu-id="a835c-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a835c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a835c-107">Syntax</span></span>

<span data-ttu-id="a835c-108">POLYLINE (\* \* *tipoDex* \* \*, \* \* *tipoDeY* \* \*, \* \* *x1* \* \*, \* \* *Y1* \* \*...)</span><span class="sxs-lookup"><span data-stu-id="a835c-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a835c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a835c-109">Parameters</span></span>

|<span data-ttu-id="a835c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a835c-110">**Name**</span></span>|<span data-ttu-id="a835c-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="a835c-111">**Required/Optional**</span></span>|<span data-ttu-id="a835c-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a835c-112">**Data Type**</span></span>|<span data-ttu-id="a835c-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a835c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a835c-114">_Alguno_</span><span class="sxs-lookup"><span data-stu-id="a835c-114">_xType_</span></span> <br/> |<span data-ttu-id="a835c-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a835c-115">Required</span></span>  <br/> |<span data-ttu-id="a835c-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a835c-116">**Boolean**</span></span> <br/> |<span data-ttu-id="a835c-117">Especifica cómo interpretar los datos de entrada _x_ .</span><span class="sxs-lookup"><span data-stu-id="a835c-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="a835c-118">Si _tipoDex_ es 0, los datos de entrada _x_se interpretan como un porcentaje del ancho.</span><span class="sxs-lookup"><span data-stu-id="a835c-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="a835c-119">Si _tipoDex_ es 1, los datos de entrada _x_se interpretan como una coordenada local.</span><span class="sxs-lookup"><span data-stu-id="a835c-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="a835c-120">_tipoDeY_</span><span class="sxs-lookup"><span data-stu-id="a835c-120">_yType_</span></span> <br/> |<span data-ttu-id="a835c-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a835c-121">Required</span></span>  <br/> |<span data-ttu-id="a835c-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a835c-122">**Boolean**</span></span> <br/> |<span data-ttu-id="a835c-123">Especifica cómo interpretar los datos de entrada _y_.</span><span class="sxs-lookup"><span data-stu-id="a835c-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="a835c-124">Si el valor de _tipoDeY_ es 0, los datos de entrada de _y_se interpretan como un porcentaje del alto.</span><span class="sxs-lookup"><span data-stu-id="a835c-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="a835c-125">Si el de _tipoDeY_ es 1, los datos de entrada de _y_se interpretan como una coordenada local.</span><span class="sxs-lookup"><span data-stu-id="a835c-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="a835c-126">_1_</span><span class="sxs-lookup"><span data-stu-id="a835c-126">_x1_</span></span> <br/> |<span data-ttu-id="a835c-127">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a835c-127">Required</span></span>  <br/> |<span data-ttu-id="a835c-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="a835c-128">**Number**</span></span> <br/> | <span data-ttu-id="a835c-129">Una coordenada _x_.</span><span class="sxs-lookup"><span data-stu-id="a835c-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="a835c-130">_a1_</span><span class="sxs-lookup"><span data-stu-id="a835c-130">_y1_</span></span> <br/> |<span data-ttu-id="a835c-131">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a835c-131">Required</span></span>  <br/> |<span data-ttu-id="a835c-132">**Number**</span><span class="sxs-lookup"><span data-stu-id="a835c-132">**Number**</span></span> <br/> |<span data-ttu-id="a835c-133">Una coordenada _y_.</span><span class="sxs-lookup"><span data-stu-id="a835c-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a835c-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a835c-134">Remarks</span></span>

<span data-ttu-id="a835c-135">Para cada argumento *x* debe haber un argumento *y* ; de lo contrario, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="a835c-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a835c-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a835c-136">Example</span></span>

<span data-ttu-id="a835c-137">POLYLINE ( 0; 0; 0; 0; 0; 1; 1; 1; 1; 0; 0; 0)</span><span class="sxs-lookup"><span data-stu-id="a835c-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="a835c-138">Devuelve un rectángulo de dimensiones Ancho x Alto.</span><span class="sxs-lookup"><span data-stu-id="a835c-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

