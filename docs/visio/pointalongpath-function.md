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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348261"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="e9cbd-103">Función POINTALONGPATH</span><span class="sxs-lookup"><span data-stu-id="e9cbd-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="e9cbd-104">Devuelve las coordenadas de un punto en la ruta de acceso o desplazado de ésta.</span><span class="sxs-lookup"><span data-stu-id="e9cbd-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="e9cbd-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="e9cbd-105">Version Information</span></span>

<span data-ttu-id="e9cbd-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="e9cbd-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e9cbd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9cbd-107">Syntax</span></span>

<span data-ttu-id="e9cbd-108">POINTALONGPATH (\* \* *sección* \* \*, \* \* *viaje* \* \* \* \* *[, desplazamiento]* \* \* \* \* *[, segmento]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e9cbd-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e9cbd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9cbd-109">Parameters</span></span>

|<span data-ttu-id="e9cbd-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="e9cbd-110">**Name**</span></span>|<span data-ttu-id="e9cbd-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e9cbd-111">**Required/Optional**</span></span>|<span data-ttu-id="e9cbd-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="e9cbd-112">**Data Type**</span></span>|<span data-ttu-id="e9cbd-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e9cbd-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e9cbd-114">_section_</span><span class="sxs-lookup"><span data-stu-id="e9cbd-114">_section_</span></span> <br/> |<span data-ttu-id="e9cbd-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e9cbd-115">Required</span></span>  <br/> |<span data-ttu-id="e9cbd-116">**String**</span><span class="sxs-lookup"><span data-stu-id="e9cbd-116">**String**</span></span> <br/> |<span data-ttu-id="e9cbd-117">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="e9cbd-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="e9cbd-118">_carrera_</span><span class="sxs-lookup"><span data-stu-id="e9cbd-118">_travel_</span></span> <br/> |<span data-ttu-id="e9cbd-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e9cbd-119">Required</span></span>  <br/> |<span data-ttu-id="e9cbd-120">**Doble**</span><span class="sxs-lookup"><span data-stu-id="e9cbd-120">**Double**</span></span> <br/> |<span data-ttu-id="e9cbd-121">Porcentaje de la ruta de acceso atravesado, desde el punto inicial al punto final que identifica al punto.</span><span class="sxs-lookup"><span data-stu-id="e9cbd-121">The percentage of the path traversed, from the begin point to the end point that identifies the point.</span></span> <span data-ttu-id="e9cbd-122">Debe oscilar entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="e9cbd-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="e9cbd-123">_desplaza_</span><span class="sxs-lookup"><span data-stu-id="e9cbd-123">_offset_</span></span> <br/> |<span data-ttu-id="e9cbd-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="e9cbd-124">Optional</span></span>  <br/> |<span data-ttu-id="e9cbd-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="e9cbd-125">**Double**</span></span> <br/> |<span data-ttu-id="e9cbd-126">Distancia de desplazamiento del punto respecto de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="e9cbd-126">The distance that the point is offset from the path.</span></span> <span data-ttu-id="e9cbd-127">Para obtener más información, vea los comentarios.</span><span class="sxs-lookup"><span data-stu-id="e9cbd-127">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="e9cbd-128">_sector_</span><span class="sxs-lookup"><span data-stu-id="e9cbd-128">_segment_</span></span> <br/> |<span data-ttu-id="e9cbd-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="e9cbd-129">Optional</span></span>  <br/> |<span data-ttu-id="e9cbd-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="e9cbd-130">**Integer**</span></span> <br/> |<span data-ttu-id="e9cbd-131">Segmento basado en 1 de la ruta de acceso en el cual se van a calcular las coordenadas.</span><span class="sxs-lookup"><span data-stu-id="e9cbd-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e9cbd-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9cbd-132">Return value</span></span>

 <span data-ttu-id="e9cbd-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="e9cbd-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9cbd-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9cbd-134">Remarks</span></span>

<span data-ttu-id="e9cbd-135">Si la _sección_ o _segmento_ no existe, Microsoft Visio devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="e9cbd-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="e9cbd-136">Los valores de *desplazamiento* positivos especifican puntos a la izquierda de la dirección del recorrido.</span><span class="sxs-lookup"><span data-stu-id="e9cbd-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="e9cbd-137">Los valores de *desplazamiento* negativos especifican puntos a la derecha de la dirección del recorrido.</span><span class="sxs-lookup"><span data-stu-id="e9cbd-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="e9cbd-138">Un **punto** representa un par ordenado de coordenadas geométricas (*x,y*) como valor único.</span><span class="sxs-lookup"><span data-stu-id="e9cbd-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

