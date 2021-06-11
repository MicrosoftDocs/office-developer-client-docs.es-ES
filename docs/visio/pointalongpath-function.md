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
# <a name="pointalongpath-function"></a><span data-ttu-id="092a4-103">Función POINTALONGPATH</span><span class="sxs-lookup"><span data-stu-id="092a4-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="092a4-104">Devuelve las coordenadas de un punto en la ruta de acceso o desplazado de ésta.</span><span class="sxs-lookup"><span data-stu-id="092a4-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="092a4-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="092a4-105">Version Information</span></span>

<span data-ttu-id="092a4-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="092a4-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="092a4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="092a4-107">Syntax</span></span>

<span data-ttu-id="092a4-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="092a4-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="092a4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="092a4-109">Parameters</span></span>

|<span data-ttu-id="092a4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="092a4-110">**Name**</span></span>|<span data-ttu-id="092a4-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="092a4-111">**Required/Optional**</span></span>|<span data-ttu-id="092a4-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="092a4-112">**Data Type**</span></span>|<span data-ttu-id="092a4-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="092a4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="092a4-114">_section_</span><span class="sxs-lookup"><span data-stu-id="092a4-114">_section_</span></span> <br/> |<span data-ttu-id="092a4-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="092a4-115">Required</span></span>  <br/> |<span data-ttu-id="092a4-116">**String**</span><span class="sxs-lookup"><span data-stu-id="092a4-116">**String**</span></span> <br/> |<span data-ttu-id="092a4-117">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="092a4-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="092a4-118">_viajes_</span><span class="sxs-lookup"><span data-stu-id="092a4-118">_travel_</span></span> <br/> |<span data-ttu-id="092a4-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="092a4-119">Required</span></span>  <br/> |<span data-ttu-id="092a4-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="092a4-120">**Double**</span></span> <br/> |<span data-ttu-id="092a4-p101">Porcentaje de la ruta de acceso atravesado, desde el punto inicial al punto final que identifica al punto. Debe oscilar entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="092a4-p101">The percentage of the path traversed, from the begin point to the end point that identifies the point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="092a4-123">_desplazamiento_</span><span class="sxs-lookup"><span data-stu-id="092a4-123">_offset_</span></span> <br/> |<span data-ttu-id="092a4-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="092a4-124">Optional</span></span>  <br/> |<span data-ttu-id="092a4-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="092a4-125">**Double**</span></span> <br/> |<span data-ttu-id="092a4-p102">Distancia de desplazamiento del punto respecto de la ruta de acceso. Para obtener más información, vea los comentarios.</span><span class="sxs-lookup"><span data-stu-id="092a4-p102">The distance that the point is offset from the path. See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="092a4-128">_segmentos_</span><span class="sxs-lookup"><span data-stu-id="092a4-128">_segment_</span></span> <br/> |<span data-ttu-id="092a4-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="092a4-129">Optional</span></span>  <br/> |<span data-ttu-id="092a4-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="092a4-130">**Integer**</span></span> <br/> |<span data-ttu-id="092a4-131">Segmento basado en 1 de la ruta de acceso en el cual se van a calcular las coordenadas.</span><span class="sxs-lookup"><span data-stu-id="092a4-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="092a4-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="092a4-132">Return value</span></span>

 <span data-ttu-id="092a4-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="092a4-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="092a4-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="092a4-134">Remarks</span></span>

<span data-ttu-id="092a4-135">Si _la_ sección o _segmento_ no existe, Microsoft Visio devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="092a4-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="092a4-136">Los  *valores de*  desplazamiento positivos especifican puntos a la izquierda de la dirección de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="092a4-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="092a4-137">Los  *valores de*  desplazamiento negativos especifican puntos a la derecha de la dirección de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="092a4-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="092a4-138">Un **punto** representa un par ordenado de coordenadas geométricas (*x,y*) como valor único.</span><span class="sxs-lookup"><span data-stu-id="092a4-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

