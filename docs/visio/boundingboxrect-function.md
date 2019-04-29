---
title: BOUNDINGBOXRECT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Devuelve la coordenada del borde especificado del cuadro de límite de la forma.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418074"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="5f626-103">Función BOUNDINGBOXRECT</span><span class="sxs-lookup"><span data-stu-id="5f626-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="5f626-104">Devuelve la coordenada del borde especificado del cuadro de límite de la forma.</span><span class="sxs-lookup"><span data-stu-id="5f626-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="5f626-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="5f626-105">Version Information</span></span>

<span data-ttu-id="5f626-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="5f626-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5f626-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f626-107">Syntax</span></span>

<span data-ttu-id="5f626-108">BOUNDINGBOXRECT (\* \* *Índice* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5f626-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5f626-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f626-109">Parameters</span></span>

|<span data-ttu-id="5f626-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5f626-110">**Name**</span></span>|<span data-ttu-id="5f626-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="5f626-111">**Required/Optional**</span></span>|<span data-ttu-id="5f626-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5f626-112">**Data Type**</span></span>|<span data-ttu-id="5f626-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f626-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5f626-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="5f626-114">_Index_</span></span> <br/> |<span data-ttu-id="5f626-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5f626-115">Required</span></span>  <br/> |<span data-ttu-id="5f626-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="5f626-116">**Integer**</span></span> <br/> |<span data-ttu-id="5f626-117">Borde del cuadro de límite de la forma del cual se va a obtener la coordenada.</span><span class="sxs-lookup"><span data-stu-id="5f626-117">The edge of the shape's bounding box for which to get the coordinate.</span></span> <span data-ttu-id="5f626-118">Vea los comentarios para conocer los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="5f626-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5f626-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f626-119">Return value</span></span>

 <span data-ttu-id="5f626-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="5f626-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f626-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f626-121">Remarks</span></span>

 <span data-ttu-id="5f626-122">*Index* puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="5f626-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="5f626-123">**Item**</span><span class="sxs-lookup"><span data-stu-id="5f626-123">**Item**</span></span>|<span data-ttu-id="5f626-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5f626-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f626-125">Borde izquierdo</span><span class="sxs-lookup"><span data-stu-id="5f626-125">Left edge</span></span>  <br/> |<span data-ttu-id="5f626-126">comprendi</span><span class="sxs-lookup"><span data-stu-id="5f626-126">0</span></span>  <br/> |
|<span data-ttu-id="5f626-127">Borde derecho</span><span class="sxs-lookup"><span data-stu-id="5f626-127">Right edge</span></span>  <br/> |<span data-ttu-id="5f626-128">1</span><span class="sxs-lookup"><span data-stu-id="5f626-128">1</span></span>  <br/> |
|<span data-ttu-id="5f626-129">Borde superior</span><span class="sxs-lookup"><span data-stu-id="5f626-129">Top edge</span></span>  <br/> |<span data-ttu-id="5f626-130">segundo</span><span class="sxs-lookup"><span data-stu-id="5f626-130">2</span></span>  <br/> |
|<span data-ttu-id="5f626-131">Borde inferior</span><span class="sxs-lookup"><span data-stu-id="5f626-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="5f626-132">3</span><span class="sxs-lookup"><span data-stu-id="5f626-132">3</span></span>  <br/> |
   
<span data-ttu-id="5f626-133">Si la forma tiene un elemento primario, el valor devuelto está en el sistema de coordenadas de dicho elemento primario.</span><span class="sxs-lookup"><span data-stu-id="5f626-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

