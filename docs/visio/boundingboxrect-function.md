---
title: BOUNDINGBOXRECT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Devuelve la coordenada del borde especificado del cuadro de límite de la forma.
ms.openlocfilehash: 2c850cb213ec0093ead53cd860f92e38da46f27e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821682"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="3070f-103">Función BOUNDINGBOXRECT</span><span class="sxs-lookup"><span data-stu-id="3070f-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="3070f-104">Devuelve la coordenada del borde especificado del cuadro de límite de la forma.</span><span class="sxs-lookup"><span data-stu-id="3070f-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="3070f-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="3070f-105">Version Information</span></span>

<span data-ttu-id="3070f-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="3070f-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3070f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3070f-107">Syntax</span></span>

<span data-ttu-id="3070f-108">BOUNDINGBOXRECT (** *índice* **)</span><span class="sxs-lookup"><span data-stu-id="3070f-108">BOUNDINGBOXRECT(** *Index* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3070f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3070f-109">Parameters</span></span>

|<span data-ttu-id="3070f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="3070f-110">**Name**</span></span>|<span data-ttu-id="3070f-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="3070f-111">**Required/Optional**</span></span>|<span data-ttu-id="3070f-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="3070f-112">**Data Type**</span></span>|<span data-ttu-id="3070f-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3070f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3070f-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="3070f-114">_Index_</span></span> <br/> |<span data-ttu-id="3070f-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3070f-115">Required</span></span>  <br/> |<span data-ttu-id="3070f-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="3070f-116">**Integer**</span></span> <br/> |<span data-ttu-id="3070f-p101">Borde del cuadro de límite de la forma del cual se va a obtener la coordenada. Vea los comentarios para conocer los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="3070f-p101">The edge of the shape's bounding box for which to get the coordinate. See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3070f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3070f-119">Return value</span></span>

 <span data-ttu-id="3070f-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="3070f-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3070f-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3070f-121">Remarks</span></span>

 <span data-ttu-id="3070f-122">*Índice* puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3070f-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="3070f-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="3070f-123">**Item**</span></span>|<span data-ttu-id="3070f-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3070f-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3070f-125">Borde izquierdo</span><span class="sxs-lookup"><span data-stu-id="3070f-125">Left edge</span></span>  <br/> |<span data-ttu-id="3070f-126">0</span><span class="sxs-lookup"><span data-stu-id="3070f-126">0</span></span>  <br/> |
|<span data-ttu-id="3070f-127">Borde derecho</span><span class="sxs-lookup"><span data-stu-id="3070f-127">Right edge</span></span>  <br/> |<span data-ttu-id="3070f-128">1</span><span class="sxs-lookup"><span data-stu-id="3070f-128">1</span></span>  <br/> |
|<span data-ttu-id="3070f-129">Borde superior</span><span class="sxs-lookup"><span data-stu-id="3070f-129">Top edge</span></span>  <br/> |<span data-ttu-id="3070f-130">2</span><span class="sxs-lookup"><span data-stu-id="3070f-130">2</span></span>  <br/> |
|<span data-ttu-id="3070f-131">Borde inferior</span><span class="sxs-lookup"><span data-stu-id="3070f-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="3070f-132">3</span><span class="sxs-lookup"><span data-stu-id="3070f-132">3</span></span>  <br/> |
   
<span data-ttu-id="3070f-133">Si la forma tiene un elemento primario, el valor devuelto está en el sistema de coordenadas de dicho elemento primario.</span><span class="sxs-lookup"><span data-stu-id="3070f-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

