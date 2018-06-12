---
title: BOUNDINGBOXDIST (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Devuelve la medida de la parte especificada del cuadro de límite de la forma.
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821687"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="c7a7e-103">BOUNDINGBOXDIST (función)</span><span class="sxs-lookup"><span data-stu-id="c7a7e-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="c7a7e-104">Devuelve la medida de la parte especificada del cuadro de límite de la forma.</span><span class="sxs-lookup"><span data-stu-id="c7a7e-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="c7a7e-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="c7a7e-105">Version Information</span></span>

<span data-ttu-id="c7a7e-106">Versión agregada: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="c7a7e-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c7a7e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7a7e-107">Syntax</span></span>

<span data-ttu-id="c7a7e-108">BOUNDINGBOXDIST (** *índice* **)</span><span class="sxs-lookup"><span data-stu-id="c7a7e-108">BOUNDINGBOXDIST(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c7a7e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7a7e-109">Parameters</span></span>

|<span data-ttu-id="c7a7e-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="c7a7e-110">**Name**</span></span>|<span data-ttu-id="c7a7e-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="c7a7e-111">**Required/Optional**</span></span>|<span data-ttu-id="c7a7e-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c7a7e-112">**Data Type**</span></span>|<span data-ttu-id="c7a7e-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7a7e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c7a7e-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="c7a7e-114">_Index_</span></span> <br/> |<span data-ttu-id="c7a7e-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c7a7e-115">Required</span></span>  <br/> |<span data-ttu-id="c7a7e-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="c7a7e-116">**Number**</span></span> <br/> |<span data-ttu-id="c7a7e-117">La parte de la forma cuadro de límite para medir y volver.</span><span class="sxs-lookup"><span data-stu-id="c7a7e-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="c7a7e-118">Vea los comentarios para conocer los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="c7a7e-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c7a7e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7a7e-119">Return value</span></span>

 <span data-ttu-id="c7a7e-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="c7a7e-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7a7e-121">Notas</span><span class="sxs-lookup"><span data-stu-id="c7a7e-121">Remarks</span></span>

 <span data-ttu-id="c7a7e-122">*Índice* puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c7a7e-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="c7a7e-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="c7a7e-123">**Item**</span></span>|<span data-ttu-id="c7a7e-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c7a7e-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7a7e-125">Ancho</span><span class="sxs-lookup"><span data-stu-id="c7a7e-125">Width</span></span>  <br/> |<span data-ttu-id="c7a7e-126">0</span><span class="sxs-lookup"><span data-stu-id="c7a7e-126">0</span></span>  <br/> |
|<span data-ttu-id="c7a7e-127">Alto</span><span class="sxs-lookup"><span data-stu-id="c7a7e-127">Height</span></span>  <br/> |<span data-ttu-id="c7a7e-128">1</span><span class="sxs-lookup"><span data-stu-id="c7a7e-128">1</span></span>  <br/> |
|<span data-ttu-id="c7a7e-129">Borde izquierdo a eje de la forma</span><span class="sxs-lookup"><span data-stu-id="c7a7e-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="c7a7e-130">2</span><span class="sxs-lookup"><span data-stu-id="c7a7e-130">2</span></span>  <br/> |
|<span data-ttu-id="c7a7e-131">Eje de la forma a borde derecho</span><span class="sxs-lookup"><span data-stu-id="c7a7e-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="c7a7e-132">3</span><span class="sxs-lookup"><span data-stu-id="c7a7e-132">3</span></span>  <br/> |
|<span data-ttu-id="c7a7e-133">Eje de la forma a borde superior</span><span class="sxs-lookup"><span data-stu-id="c7a7e-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="c7a7e-134">4</span><span class="sxs-lookup"><span data-stu-id="c7a7e-134">4</span></span>  <br/> |
|<span data-ttu-id="c7a7e-135">Borde inferior a eje de la forma</span><span class="sxs-lookup"><span data-stu-id="c7a7e-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="c7a7e-136">5</span><span class="sxs-lookup"><span data-stu-id="c7a7e-136">5</span></span>  <br/> |
|<span data-ttu-id="c7a7e-137">Centro del cuadro de límite a EjeX</span><span class="sxs-lookup"><span data-stu-id="c7a7e-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="c7a7e-138">6</span><span class="sxs-lookup"><span data-stu-id="c7a7e-138">6</span></span>  <br/> |
|<span data-ttu-id="c7a7e-139">Centro del cuadro de límite a EjeY</span><span class="sxs-lookup"><span data-stu-id="c7a7e-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="c7a7e-140">7</span><span class="sxs-lookup"><span data-stu-id="c7a7e-140">7</span></span>  <br/> |
   

