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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348968"
---
# <a name="boundingboxdist-function"></a><span data-ttu-id="75ed5-103">Función BOUNDINGBOXDIST</span><span class="sxs-lookup"><span data-stu-id="75ed5-103">BOUNDINGBOXDIST Function</span></span>

<span data-ttu-id="75ed5-104">Devuelve la medida de la parte especificada del cuadro de límite de la forma.</span><span class="sxs-lookup"><span data-stu-id="75ed5-104">Returns the measurement of the specified part of the shape's bounding box.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="75ed5-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="75ed5-105">Version Information</span></span>

<span data-ttu-id="75ed5-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="75ed5-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="75ed5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75ed5-107">Syntax</span></span>

<span data-ttu-id="75ed5-108">BOUNDINGBOXDIST (\* \* *Índice* \* \*)</span><span class="sxs-lookup"><span data-stu-id="75ed5-108">BOUNDINGBOXDIST(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="75ed5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75ed5-109">Parameters</span></span>

|<span data-ttu-id="75ed5-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="75ed5-110">**Name**</span></span>|<span data-ttu-id="75ed5-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="75ed5-111">**Required/Optional**</span></span>|<span data-ttu-id="75ed5-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="75ed5-112">**Data Type**</span></span>|<span data-ttu-id="75ed5-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="75ed5-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="75ed5-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="75ed5-114">_Index_</span></span> <br/> |<span data-ttu-id="75ed5-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="75ed5-115">Required</span></span>  <br/> |<span data-ttu-id="75ed5-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="75ed5-116">**Number**</span></span> <br/> |<span data-ttu-id="75ed5-117">Parte del cuadro de límite de la forma que se va a medir y devolver.</span><span class="sxs-lookup"><span data-stu-id="75ed5-117">The part of the shape's bounding box to measure and return.</span></span> <span data-ttu-id="75ed5-118">Vea la sección Comentarios para los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="75ed5-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="75ed5-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75ed5-119">Return value</span></span>

 <span data-ttu-id="75ed5-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="75ed5-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75ed5-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="75ed5-121">Remarks</span></span>

 <span data-ttu-id="75ed5-122">*Index* puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="75ed5-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="75ed5-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="75ed5-123">**Item**</span></span>|<span data-ttu-id="75ed5-124">**Value**</span><span class="sxs-lookup"><span data-stu-id="75ed5-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75ed5-125">Width</span><span class="sxs-lookup"><span data-stu-id="75ed5-125">Width</span></span>  <br/> |<span data-ttu-id="75ed5-126">comprendi</span><span class="sxs-lookup"><span data-stu-id="75ed5-126">0</span></span>  <br/> |
|<span data-ttu-id="75ed5-127">Height</span><span class="sxs-lookup"><span data-stu-id="75ed5-127">Height</span></span>  <br/> |<span data-ttu-id="75ed5-128">1</span><span class="sxs-lookup"><span data-stu-id="75ed5-128">1</span></span>  <br/> |
|<span data-ttu-id="75ed5-129">Borde izquierdo a eje de la forma</span><span class="sxs-lookup"><span data-stu-id="75ed5-129">Left edge to shape pin</span></span>  <br/> |<span data-ttu-id="75ed5-130">segundo</span><span class="sxs-lookup"><span data-stu-id="75ed5-130">2</span></span>  <br/> |
|<span data-ttu-id="75ed5-131">Eje de la forma a borde derecho</span><span class="sxs-lookup"><span data-stu-id="75ed5-131">Shape pin to right edge</span></span>  <br/> |<span data-ttu-id="75ed5-132">3</span><span class="sxs-lookup"><span data-stu-id="75ed5-132">3</span></span>  <br/> |
|<span data-ttu-id="75ed5-133">Eje de la forma a borde superior</span><span class="sxs-lookup"><span data-stu-id="75ed5-133">Shape pin to top edge</span></span>  <br/> |<span data-ttu-id="75ed5-134">4</span><span class="sxs-lookup"><span data-stu-id="75ed5-134">4</span></span>  <br/> |
|<span data-ttu-id="75ed5-135">Borde inferior a eje de la forma</span><span class="sxs-lookup"><span data-stu-id="75ed5-135">Bottom edge to shape pin</span></span>  <br/> |<span data-ttu-id="75ed5-136">2,5</span><span class="sxs-lookup"><span data-stu-id="75ed5-136">5</span></span>  <br/> |
|<span data-ttu-id="75ed5-137">Centro del cuadro de límite a EjeX</span><span class="sxs-lookup"><span data-stu-id="75ed5-137">Center of bounding box to PinX</span></span>  <br/> |<span data-ttu-id="75ed5-138">6,5</span><span class="sxs-lookup"><span data-stu-id="75ed5-138">6</span></span>  <br/> |
|<span data-ttu-id="75ed5-139">Centro del cuadro de límite a EjeY</span><span class="sxs-lookup"><span data-stu-id="75ed5-139">Center of bounding box to PinY</span></span>  <br/> |<span data-ttu-id="75ed5-140">0,7</span><span class="sxs-lookup"><span data-stu-id="75ed5-140">7</span></span>  <br/> |
   

