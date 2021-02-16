---
title: ANGLEALONGPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Devuelve el ángulo de la tangente a la ruta de acceso en un punto dado.
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160296"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="3cc98-103">Función ANGLEALONGPATH</span><span class="sxs-lookup"><span data-stu-id="3cc98-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="3cc98-104">Devuelve el ángulo de la tangente a la ruta de acceso en un punto dado.</span><span class="sxs-lookup"><span data-stu-id="3cc98-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="3cc98-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="3cc98-105">Version Information</span></span>

<span data-ttu-id="3cc98-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="3cc98-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3cc98-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3cc98-107">Syntax</span></span>

<span data-ttu-id="3cc98-108">ANGLEALONGPATH(***section***, ***travel*** ***[,segment]*** )</span><span class="sxs-lookup"><span data-stu-id="3cc98-108">ANGLEALONGPATH(***section***, ***travel*** ***[,segment]*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3cc98-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3cc98-109">Parameters</span></span>

|<span data-ttu-id="3cc98-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="3cc98-110">**Name**</span></span>|<span data-ttu-id="3cc98-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="3cc98-111">**Required/Optional**</span></span>|<span data-ttu-id="3cc98-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="3cc98-112">**Data Type**</span></span>|<span data-ttu-id="3cc98-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3cc98-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3cc98-114">_section_</span><span class="sxs-lookup"><span data-stu-id="3cc98-114">_section_</span></span> <br/> |<span data-ttu-id="3cc98-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3cc98-115">Required</span></span>  <br/> |<span data-ttu-id="3cc98-116">**String**</span><span class="sxs-lookup"><span data-stu-id="3cc98-116">**String**</span></span> <br/> |<span data-ttu-id="3cc98-117">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="3cc98-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="3cc98-118">_travel_</span><span class="sxs-lookup"><span data-stu-id="3cc98-118">_travel_</span></span> <br/> |<span data-ttu-id="3cc98-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="3cc98-119">Required</span></span>  <br/> |<span data-ttu-id="3cc98-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="3cc98-120">**Double**</span></span> <br/> |<span data-ttu-id="3cc98-121">Porcentaje a lo largo de la ruta de acceso, desde el punto inicial hasta el punto final.</span><span class="sxs-lookup"><span data-stu-id="3cc98-121">The percentage along the path from begin point to end point.</span></span> <span data-ttu-id="3cc98-122">Debe ser un valor entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="3cc98-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="3cc98-123">_segmentos_</span><span class="sxs-lookup"><span data-stu-id="3cc98-123">_segment_</span></span> <br/> |<span data-ttu-id="3cc98-124">Opcional</span><span class="sxs-lookup"><span data-stu-id="3cc98-124">Optional</span></span>  <br/> |<span data-ttu-id="3cc98-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="3cc98-125">**Integer**</span></span> <br/> |<span data-ttu-id="3cc98-126">Segmento basado en 1 de la ruta de acceso en el cual se calcula el ángulo de la tangente.</span><span class="sxs-lookup"><span data-stu-id="3cc98-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3cc98-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3cc98-127">Return value</span></span>

 <span data-ttu-id="3cc98-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="3cc98-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3cc98-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3cc98-129">Remarks</span></span>

<span data-ttu-id="3cc98-130">Si incluye un valor  _de segmento,_ ANGLEALONGPATH solo devuelve el valor de ese segmento.</span><span class="sxs-lookup"><span data-stu-id="3cc98-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="3cc98-131">Si incluye un valor _de_ segmento, ANGLEALONGPATH determina el  punto de la tangente mediante viajes para calcular la percertage a lo largo del _segmento_.</span><span class="sxs-lookup"><span data-stu-id="3cc98-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="3cc98-132">Si no  _existe ninguna_  _sección_ o segmento, Microsoft Visio devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="3cc98-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

