---
title: ANGLEALONGPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Devuelve el ángulo de la tangente a la ruta de acceso en un punto dado.
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821551"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="5be4d-103">ANGLEALONGPATH (función)</span><span class="sxs-lookup"><span data-stu-id="5be4d-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="5be4d-104">Devuelve el ángulo de la tangente a la ruta de acceso en un punto dado.</span><span class="sxs-lookup"><span data-stu-id="5be4d-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="5be4d-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="5be4d-105">Version Information</span></span>

<span data-ttu-id="5be4d-106">Versión agregada: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="5be4d-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5be4d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5be4d-107">Syntax</span></span>

<span data-ttu-id="5be4d-108">ANGLEALONGPATH (** *sección* **, ** *viajes* ** ** *[, segmento]* **)</span><span class="sxs-lookup"><span data-stu-id="5be4d-108">ANGLEALONGPATH(** *section* **, ** *travel* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5be4d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5be4d-109">Parameters</span></span>

|<span data-ttu-id="5be4d-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="5be4d-110">**Name**</span></span>|<span data-ttu-id="5be4d-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="5be4d-111">**Required/Optional**</span></span>|<span data-ttu-id="5be4d-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5be4d-112">**Data Type**</span></span>|<span data-ttu-id="5be4d-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5be4d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5be4d-114">_section_</span><span class="sxs-lookup"><span data-stu-id="5be4d-114">_section_</span></span> <br/> |<span data-ttu-id="5be4d-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5be4d-115">Required</span></span>  <br/> |<span data-ttu-id="5be4d-116">**String**</span><span class="sxs-lookup"><span data-stu-id="5be4d-116">**String**</span></span> <br/> |<span data-ttu-id="5be4d-117">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="5be4d-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="5be4d-118">_viajes_</span><span class="sxs-lookup"><span data-stu-id="5be4d-118">_travel_</span></span> <br/> |<span data-ttu-id="5be4d-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5be4d-119">Required</span></span>  <br/> |<span data-ttu-id="5be4d-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="5be4d-120">**Double**</span></span> <br/> |<span data-ttu-id="5be4d-p101">Porcentaje a lo largo de la ruta de acceso, desde el punto inicial hasta el punto final. Debe ser un valor entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="5be4d-p101">The percentage along the path from begin point to end point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="5be4d-123">_segmento_</span><span class="sxs-lookup"><span data-stu-id="5be4d-123">_segment_</span></span> <br/> |<span data-ttu-id="5be4d-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="5be4d-124">Optional</span></span>  <br/> |<span data-ttu-id="5be4d-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="5be4d-125">**Integer**</span></span> <br/> |<span data-ttu-id="5be4d-126">Segmento basado en 1 de la ruta de acceso en el cual se calcula el ángulo de la tangente.</span><span class="sxs-lookup"><span data-stu-id="5be4d-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5be4d-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5be4d-127">Return value</span></span>

 <span data-ttu-id="5be4d-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="5be4d-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5be4d-129">Notas</span><span class="sxs-lookup"><span data-stu-id="5be4d-129">Remarks</span></span>

<span data-ttu-id="5be4d-130">Si incluye un valor _segment_ , ANGLEALONGPATH devuelve el valor solamente para ese segmento.</span><span class="sxs-lookup"><span data-stu-id="5be4d-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="5be4d-131">Si incluye un valor _segment_ , ANGLEALONGPATH determina el punto de la tangente mediante el uso _de viajes_ para calcular la percertage a lo largo de _segmento_.</span><span class="sxs-lookup"><span data-stu-id="5be4d-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="5be4d-132">Si no existe _section_ ni _segment_ , Microsoft Visio devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="5be4d-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

