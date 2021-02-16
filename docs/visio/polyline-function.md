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
description: Devuelve una polilínea. Esta función se usa en la celda A de las filas de geometría PolyLineTo.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426299"
---
# <a name="polyline-function"></a><span data-ttu-id="efcf5-104">Función POLYLINE</span><span class="sxs-lookup"><span data-stu-id="efcf5-104">POLYLINE Function</span></span>

<span data-ttu-id="efcf5-105">Devuelve una polilínea.</span><span class="sxs-lookup"><span data-stu-id="efcf5-105">Returns a polyline.</span></span> <span data-ttu-id="efcf5-106">Esta función se usa en la celda A de las filas de geometría PolyLineTo.</span><span class="sxs-lookup"><span data-stu-id="efcf5-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="efcf5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efcf5-107">Syntax</span></span>

<span data-ttu-id="efcf5-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span><span class="sxs-lookup"><span data-stu-id="efcf5-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="efcf5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efcf5-109">Parameters</span></span>

|<span data-ttu-id="efcf5-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="efcf5-110">**Name**</span></span>|<span data-ttu-id="efcf5-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="efcf5-111">**Required/Optional**</span></span>|<span data-ttu-id="efcf5-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="efcf5-112">**Data Type**</span></span>|<span data-ttu-id="efcf5-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="efcf5-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="efcf5-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="efcf5-114">_xType_</span></span> <br/> |<span data-ttu-id="efcf5-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="efcf5-115">Required</span></span>  <br/> |<span data-ttu-id="efcf5-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="efcf5-116">**Boolean**</span></span> <br/> |<span data-ttu-id="efcf5-117">Especifica cómo interpretar los datos _de entrada x._</span><span class="sxs-lookup"><span data-stu-id="efcf5-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="efcf5-118">Si  _xType_ es 0, la  _entrada x_-data se interpreta como un porcentaje de Width.</span><span class="sxs-lookup"><span data-stu-id="efcf5-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="efcf5-119">Si  _xType_ es 1, la  _entrada x_-data se interpreta como una coordenada local.</span><span class="sxs-lookup"><span data-stu-id="efcf5-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="efcf5-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="efcf5-120">_yType_</span></span> <br/> |<span data-ttu-id="efcf5-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="efcf5-121">Required</span></span>  <br/> |<span data-ttu-id="efcf5-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="efcf5-122">**Boolean**</span></span> <br/> |<span data-ttu-id="efcf5-123">Especifica cómo interpretar los datos _de y-input._</span><span class="sxs-lookup"><span data-stu-id="efcf5-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="efcf5-124">Si  _yType_ es 0, la  _entrada y_-data se interpreta como un porcentaje de Height.</span><span class="sxs-lookup"><span data-stu-id="efcf5-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="efcf5-125">Si  _yType_ es 1, la  _entrada y_-data se interpreta como una coordenada local.</span><span class="sxs-lookup"><span data-stu-id="efcf5-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="efcf5-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="efcf5-126">_x1_</span></span> <br/> |<span data-ttu-id="efcf5-127">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="efcf5-127">Required</span></span>  <br/> |<span data-ttu-id="efcf5-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="efcf5-128">**Number**</span></span> <br/> | <span data-ttu-id="efcf5-129">_Coordenada x._</span><span class="sxs-lookup"><span data-stu-id="efcf5-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="efcf5-130">_y1_</span><span class="sxs-lookup"><span data-stu-id="efcf5-130">_y1_</span></span> <br/> |<span data-ttu-id="efcf5-131">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="efcf5-131">Required</span></span>  <br/> |<span data-ttu-id="efcf5-132">**Number**</span><span class="sxs-lookup"><span data-stu-id="efcf5-132">**Number**</span></span> <br/> |<span data-ttu-id="efcf5-133">_Coordenada y._</span><span class="sxs-lookup"><span data-stu-id="efcf5-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efcf5-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="efcf5-134">Remarks</span></span>

<span data-ttu-id="efcf5-135">Para cada  *argumento x,*  debe haber un  *argumento y;*  de lo contrario, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="efcf5-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="efcf5-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="efcf5-136">Example</span></span>

<span data-ttu-id="efcf5-137">POLYLINE ( 0; 0; 0; 0; 0; 1; 1; 1; 1; 0; 0; 0)</span><span class="sxs-lookup"><span data-stu-id="efcf5-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="efcf5-138">Devuelve un rectángulo de dimensiones Ancho x Alto.</span><span class="sxs-lookup"><span data-stu-id="efcf5-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

