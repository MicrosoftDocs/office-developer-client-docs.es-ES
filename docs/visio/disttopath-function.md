---
title: DISTTOPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Devuelve la distancia más corta desde el punto representado por las coordenadas especificadas a un punto en la ruta de acceso.
ms.openlocfilehash: 227fe860de2e3683b5d7d3e5f9313d1e2e31b2d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822009"
---
# <a name="disttopath-function"></a><span data-ttu-id="a74e3-103">Función DISTTOPATH</span><span class="sxs-lookup"><span data-stu-id="a74e3-103">DISTTOPATH Function</span></span>

<span data-ttu-id="a74e3-104">Devuelve la distancia más corta desde el punto representado por las coordenadas especificadas a un punto en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a74e3-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="a74e3-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="a74e3-105">Version Information</span></span>

<span data-ttu-id="a74e3-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="a74e3-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a74e3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a74e3-107">Syntax</span></span>

<span data-ttu-id="a74e3-108">DISTTOPATH (** *sección* **, ** *x* **, ** *y* **)</span><span class="sxs-lookup"><span data-stu-id="a74e3-108">DISTTOPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a74e3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a74e3-109">Parameters</span></span>

|<span data-ttu-id="a74e3-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a74e3-110">**Name**</span></span>|<span data-ttu-id="a74e3-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="a74e3-111">**Required/Optional**</span></span>|<span data-ttu-id="a74e3-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a74e3-112">**Data Type**</span></span>|<span data-ttu-id="a74e3-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a74e3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a74e3-114">_section_</span><span class="sxs-lookup"><span data-stu-id="a74e3-114">_section_</span></span> <br/> |<span data-ttu-id="a74e3-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a74e3-115">Required</span></span>  <br/> |<span data-ttu-id="a74e3-116">**String**</span><span class="sxs-lookup"><span data-stu-id="a74e3-116">**String**</span></span> <br/> |<span data-ttu-id="a74e3-117">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="a74e3-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="a74e3-118">_x_</span><span class="sxs-lookup"><span data-stu-id="a74e3-118">_x_</span></span> <br/> |<span data-ttu-id="a74e3-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a74e3-119">Required</span></span>  <br/> |<span data-ttu-id="a74e3-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="a74e3-120">**Double**</span></span> <br/> |<span data-ttu-id="a74e3-121">La _x_-coordenadas del punto.</span><span class="sxs-lookup"><span data-stu-id="a74e3-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="a74e3-122">_y_</span><span class="sxs-lookup"><span data-stu-id="a74e3-122">_y_</span></span> <br/> |<span data-ttu-id="a74e3-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a74e3-123">Required</span></span>  <br/> |<span data-ttu-id="a74e3-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="a74e3-124">**Double**</span></span> <br/> |<span data-ttu-id="a74e3-125">La _y_-coordenadas del punto.</span><span class="sxs-lookup"><span data-stu-id="a74e3-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a74e3-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a74e3-126">Return value</span></span>

 <span data-ttu-id="a74e3-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="a74e3-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a74e3-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a74e3-128">Remarks</span></span>

<span data-ttu-id="a74e3-129">¡Microsoft Visio devuelve #REF!</span><span class="sxs-lookup"><span data-stu-id="a74e3-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="a74e3-130">Si no existe la _sección_ .</span><span class="sxs-lookup"><span data-stu-id="a74e3-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="a74e3-131">El valor devuelto es positivo si el punto se encuentra a la izquierda de la dirección del recorrido y negativo si se encuentra a la derecha.</span><span class="sxs-lookup"><span data-stu-id="a74e3-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

