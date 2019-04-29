---
title: BOUNDINGBOXDIST (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Devuelve la medida de la parte especificada del cuadro de límite de la forma.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428280"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="c4412-103">Función BOUNDINGBOXDIST</span><span class="sxs-lookup"><span data-stu-id="c4412-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="c4412-104">Devuelve la medida de la parte especificada del cuadro de límite de la forma.</span><span class="sxs-lookup"><span data-stu-id="c4412-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="c4412-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="c4412-105">Version Information</span></span>

<span data-ttu-id="c4412-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="c4412-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c4412-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4412-107">Syntax</span></span>

<span data-ttu-id="c4412-108">BOUNDINGBOXDIST (\* \* *Índice* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c4412-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c4412-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4412-109">Parameters</span></span>

|<span data-ttu-id="c4412-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4412-110">**Name**</span></span>|<span data-ttu-id="c4412-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c4412-111">**Required/Optional**</span></span>|<span data-ttu-id="c4412-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c4412-112">**Data Type**</span></span>|<span data-ttu-id="c4412-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4412-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c4412-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="c4412-114">_Index_</span></span> <br/> |<span data-ttu-id="c4412-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="c4412-115">Required</span></span>  <br/> |<span data-ttu-id="c4412-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="c4412-116">**Number**</span></span> <br/> |<span data-ttu-id="c4412-117">Parte del cuadro de límite de la forma que se va a medir y devolver.</span><span class="sxs-lookup"><span data-stu-id="c4412-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="c4412-118">Vea la sección Comentarios para los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="c4412-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c4412-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4412-119">Return value</span></span>

 <span data-ttu-id="c4412-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="c4412-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4412-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4412-121">Remarks</span></span>

 <span data-ttu-id="c4412-122">*Index* puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="c4412-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="c4412-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="c4412-123">**Item**</span></span>|<span data-ttu-id="c4412-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c4412-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4412-125">Width</span><span class="sxs-lookup"><span data-stu-id="c4412-125">Width</span></span>  <br/> |<span data-ttu-id="c4412-126">comprendi</span><span class="sxs-lookup"><span data-stu-id="c4412-126">0</span></span>  <br/> |
|<span data-ttu-id="c4412-127">Height</span><span class="sxs-lookup"><span data-stu-id="c4412-127">Height</span></span>  <br/> |<span data-ttu-id="c4412-128">1</span><span class="sxs-lookup"><span data-stu-id="c4412-128">1</span></span>  <br/> |
|<span data-ttu-id="c4412-129">Borde izquierdo a eje de la forma</span><span class="sxs-lookup"><span data-stu-id="c4412-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="c4412-130">segundo</span><span class="sxs-lookup"><span data-stu-id="c4412-130">2</span></span>  <br/> |
|<span data-ttu-id="c4412-131">Eje de la forma a borde derecho</span><span class="sxs-lookup"><span data-stu-id="c4412-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="c4412-132">3</span><span class="sxs-lookup"><span data-stu-id="c4412-132">3</span></span>  <br/> |
|<span data-ttu-id="c4412-133">Eje de la forma a borde superior</span><span class="sxs-lookup"><span data-stu-id="c4412-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="c4412-134">4 </span><span class="sxs-lookup"><span data-stu-id="c4412-134">4</span></span>  <br/> |
|<span data-ttu-id="c4412-135">Borde inferior a eje de la forma</span><span class="sxs-lookup"><span data-stu-id="c4412-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="c4412-136">5 </span><span class="sxs-lookup"><span data-stu-id="c4412-136">5</span></span>  <br/> |
|<span data-ttu-id="c4412-137">Centro del cuadro de límite a EjeX</span><span class="sxs-lookup"><span data-stu-id="c4412-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="c4412-138">6 </span><span class="sxs-lookup"><span data-stu-id="c4412-138">6</span></span>  <br/> |
|<span data-ttu-id="c4412-139">Centro del cuadro de límite a EjeY</span><span class="sxs-lookup"><span data-stu-id="c4412-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="c4412-140">7 </span><span class="sxs-lookup"><span data-stu-id="c4412-140">7</span></span>  <br/> |
   

