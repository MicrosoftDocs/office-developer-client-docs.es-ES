---
title: NEARESTPOINTONPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Devuelve el porcentaje (como un valor entre 0 y 1) de la distancia a lo largo de la ruta de acceso del punto que se encuentra más cerca de las coordenadas especificadas.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319722"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="462e4-103">Función NEARESTPOINTONPATH</span><span class="sxs-lookup"><span data-stu-id="462e4-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="462e4-104">Devuelve el porcentaje (como un valor entre 0 y 1) de la distancia a lo largo de la ruta de acceso del punto que se encuentra más cerca de las coordenadas especificadas.</span><span class="sxs-lookup"><span data-stu-id="462e4-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="462e4-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="462e4-105">Version Information</span></span>

<span data-ttu-id="462e4-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="462e4-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="462e4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="462e4-107">Syntax</span></span>

<span data-ttu-id="462e4-108">NEARESTPOINTONPATH (\* \* *sección* \* \*, \* \* *x* \* \*, \* \* *y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="462e4-108">NEARESTPOINTONPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="462e4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="462e4-109">Parameters</span></span>

|<span data-ttu-id="462e4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="462e4-110">**Name**</span></span>|<span data-ttu-id="462e4-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="462e4-111">**Required/Optional**</span></span>|<span data-ttu-id="462e4-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="462e4-112">**Data Type**</span></span>|<span data-ttu-id="462e4-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="462e4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="462e4-114">_section_</span><span class="sxs-lookup"><span data-stu-id="462e4-114">_section_</span></span> <br/> |<span data-ttu-id="462e4-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="462e4-115">Required</span></span>  <br/> |<span data-ttu-id="462e4-116">**String**</span><span class="sxs-lookup"><span data-stu-id="462e4-116">**String**</span></span> <br/> |<span data-ttu-id="462e4-117">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="462e4-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="462e4-118">_x_</span><span class="sxs-lookup"><span data-stu-id="462e4-118">_x_</span></span> <br/> |<span data-ttu-id="462e4-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="462e4-119">Required</span></span>  <br/> |<span data-ttu-id="462e4-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="462e4-120">**Double**</span></span> <br/> |<span data-ttu-id="462e4-121">Coordenada _x_del punto especificado.</span><span class="sxs-lookup"><span data-stu-id="462e4-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="462e4-122">_y_</span><span class="sxs-lookup"><span data-stu-id="462e4-122">_y_</span></span> <br/> |<span data-ttu-id="462e4-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="462e4-123">Required</span></span>  <br/> |<span data-ttu-id="462e4-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="462e4-124">**Double**</span></span> <br/> |<span data-ttu-id="462e4-125">Coordenada _y_del punto especificado.</span><span class="sxs-lookup"><span data-stu-id="462e4-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="462e4-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="462e4-126">Return value</span></span>

 <span data-ttu-id="462e4-127">**Doble**</span><span class="sxs-lookup"><span data-stu-id="462e4-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="462e4-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="462e4-128">Remarks</span></span>

<span data-ttu-id="462e4-129">Si _section_ no existe, Microsoft Visio devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="462e4-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

