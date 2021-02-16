---
title: POINTALONGPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Devuelve las coordenadas de un punto en la ruta de acceso o desplazado de ésta.
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430486"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="9991f-103">Función POINTALONGPATH</span><span class="sxs-lookup"><span data-stu-id="9991f-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="9991f-104">Devuelve las coordenadas de un punto en la ruta de acceso o desplazado de ésta.</span><span class="sxs-lookup"><span data-stu-id="9991f-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="9991f-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="9991f-105">Version Information</span></span>

<span data-ttu-id="9991f-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="9991f-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9991f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9991f-107">Syntax</span></span>

<span data-ttu-id="9991f-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="9991f-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9991f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9991f-109">Parameters</span></span>

|<span data-ttu-id="9991f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="9991f-110">**Name**</span></span>|<span data-ttu-id="9991f-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="9991f-111">**Required/Optional**</span></span>|<span data-ttu-id="9991f-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="9991f-112">**Data Type**</span></span>|<span data-ttu-id="9991f-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9991f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9991f-114">_section_</span><span class="sxs-lookup"><span data-stu-id="9991f-114">_section_</span></span> <br/> |<span data-ttu-id="9991f-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9991f-115">Required</span></span>  <br/> |<span data-ttu-id="9991f-116">**String**</span><span class="sxs-lookup"><span data-stu-id="9991f-116">**String**</span></span> <br/> |<span data-ttu-id="9991f-117">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="9991f-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="9991f-118">_travel_</span><span class="sxs-lookup"><span data-stu-id="9991f-118">_travel_</span></span> <br/> |<span data-ttu-id="9991f-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9991f-119">Required</span></span>  <br/> |<span data-ttu-id="9991f-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="9991f-120">**Double**</span></span> <br/> |<span data-ttu-id="9991f-121">Porcentaje de la ruta de acceso atravesado, desde el punto inicial al punto final que identifica al punto.</span><span class="sxs-lookup"><span data-stu-id="9991f-121">The percentage of the path traversed, from the begin point to the end point that identifies the point.</span></span> <span data-ttu-id="9991f-122">Debe oscilar entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="9991f-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="9991f-123">_offset_</span><span class="sxs-lookup"><span data-stu-id="9991f-123">_offset_</span></span> <br/> |<span data-ttu-id="9991f-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="9991f-124">Optional</span></span>  <br/> |<span data-ttu-id="9991f-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="9991f-125">**Double**</span></span> <br/> |<span data-ttu-id="9991f-126">Distancia de desplazamiento del punto respecto de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="9991f-126">The distance that the point is offset from the path.</span></span> <span data-ttu-id="9991f-127">Para obtener más información, vea los comentarios.</span><span class="sxs-lookup"><span data-stu-id="9991f-127">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="9991f-128">_segmentos_</span><span class="sxs-lookup"><span data-stu-id="9991f-128">_segment_</span></span> <br/> |<span data-ttu-id="9991f-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="9991f-129">Optional</span></span>  <br/> |<span data-ttu-id="9991f-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="9991f-130">**Integer**</span></span> <br/> |<span data-ttu-id="9991f-131">Segmento basado en 1 de la ruta de acceso en el cual se van a calcular las coordenadas.</span><span class="sxs-lookup"><span data-stu-id="9991f-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9991f-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9991f-132">Return value</span></span>

 <span data-ttu-id="9991f-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="9991f-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9991f-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9991f-134">Remarks</span></span>

<span data-ttu-id="9991f-135">Si  _no_ existe  _una_ sección o un segmento, Microsoft Visio devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="9991f-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="9991f-136">Los  *valores de*  desplazamiento positivo especifican puntos a la izquierda de la dirección de viaje.</span><span class="sxs-lookup"><span data-stu-id="9991f-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="9991f-137">Los  *valores de*  desplazamiento negativos especifican puntos a la derecha de la dirección de viaje.</span><span class="sxs-lookup"><span data-stu-id="9991f-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="9991f-138">Un **punto** representa un par ordenado de coordenadas geométricas (*x,y*) como valor único.</span><span class="sxs-lookup"><span data-stu-id="9991f-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

