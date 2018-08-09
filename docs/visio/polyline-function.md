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
description: Devuelve una polilínea. Esta función se usa en la celda a de las filas de geometría PolyLineTo.
ms.openlocfilehash: afe31b3963cca03d0273b8768f6cc5538d1850ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822766"
---
# <a name="polyline-function"></a><span data-ttu-id="5f1a4-104">Función POLYLINE</span><span class="sxs-lookup"><span data-stu-id="5f1a4-104">POLYLINE Function</span></span>

<span data-ttu-id="5f1a4-105">Devuelve una polilínea.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-105">Returns a polyline.</span></span> <span data-ttu-id="5f1a4-106">Esta función se usa en la celda a de las filas de geometría PolyLineTo.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5f1a4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f1a4-107">Syntax</span></span>

<span data-ttu-id="5f1a4-108">POLYLINE (** *tipoDeX* **, ** *tipoDeY* **, ** *x1* **, ** *y1* **...)</span><span class="sxs-lookup"><span data-stu-id="5f1a4-108">POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5f1a4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f1a4-109">Parameters</span></span>

|<span data-ttu-id="5f1a4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5f1a4-110">**Name**</span></span>|<span data-ttu-id="5f1a4-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="5f1a4-111">**Required/Optional**</span></span>|<span data-ttu-id="5f1a4-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5f1a4-112">**Data Type**</span></span>|<span data-ttu-id="5f1a4-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f1a4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5f1a4-114">_tipoDeX_</span><span class="sxs-lookup"><span data-stu-id="5f1a4-114">_xType_</span></span> <br/> |<span data-ttu-id="5f1a4-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5f1a4-115">Required</span></span>  <br/> |<span data-ttu-id="5f1a4-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5f1a4-116">**Boolean**</span></span> <br/> |<span data-ttu-id="5f1a4-117">Especifica cómo interpretar los datos de entrada de _x_ .</span><span class="sxs-lookup"><span data-stu-id="5f1a4-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="5f1a4-118">_Si es 0, la entrada _x__ -datos x se interpretan como un porcentaje del ancho.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="5f1a4-119">_Si es 1, la entrada _x__ -datos se interpretan como una coordenada local.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="5f1a4-120">_dos valores_</span><span class="sxs-lookup"><span data-stu-id="5f1a4-120">_yType_</span></span> <br/> |<span data-ttu-id="5f1a4-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5f1a4-121">Required</span></span>  <br/> |<span data-ttu-id="5f1a4-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5f1a4-122">**Boolean**</span></span> <br/> |<span data-ttu-id="5f1a4-123">Especifica cómo se debe interpretar la _y_-datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="5f1a4-124">_Si es 0, la entrada _y__ -datos de x se interpretan como un porcentaje del alto.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="5f1a4-125">_Si es 1, la entrada _y__ -datos se interpretan como una coordenada local.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="5f1a4-126">_X1_</span><span class="sxs-lookup"><span data-stu-id="5f1a4-126">_x1_</span></span> <br/> |<span data-ttu-id="5f1a4-127">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5f1a4-127">Required</span></span>  <br/> |<span data-ttu-id="5f1a4-128">**Número**</span><span class="sxs-lookup"><span data-stu-id="5f1a4-128">**Number**</span></span> <br/> | <span data-ttu-id="5f1a4-129">Una _x_-coordinar.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="5f1a4-130">_Y1_</span><span class="sxs-lookup"><span data-stu-id="5f1a4-130">_y1_</span></span> <br/> |<span data-ttu-id="5f1a4-131">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5f1a4-131">Required</span></span>  <br/> |<span data-ttu-id="5f1a4-132">**Número**</span><span class="sxs-lookup"><span data-stu-id="5f1a4-132">**Number**</span></span> <br/> |<span data-ttu-id="5f1a4-133">Un _y_-coordinar.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f1a4-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f1a4-134">Remarks</span></span>

<span data-ttu-id="5f1a4-135">Para cada argumento *x* debe haber un argumento *y* ; de lo contrario, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5f1a4-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f1a4-136">Example</span></span>

<span data-ttu-id="5f1a4-137">POLYLINE ( 0; 0; 0; 0; 0; 1; 1; 1; 1; 0; 0; 0)</span><span class="sxs-lookup"><span data-stu-id="5f1a4-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="5f1a4-138">Devuelve un rectángulo de dimensiones Ancho x Alto.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

