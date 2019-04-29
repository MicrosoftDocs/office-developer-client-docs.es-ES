---
title: DISTTOPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Devuelve la distancia más corta desde el punto representado por las coordenadas especificadas a un punto en la ruta de acceso.
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427020"
---
# <a name="disttopath-function"></a><span data-ttu-id="687a0-103">Función DISTTOPATH</span><span class="sxs-lookup"><span data-stu-id="687a0-103">DISTTOPATH Function</span></span>

<span data-ttu-id="687a0-104">Devuelve la distancia más corta desde el punto representado por las coordenadas especificadas a un punto en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="687a0-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="687a0-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="687a0-105">Version Information</span></span>

<span data-ttu-id="687a0-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="687a0-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="687a0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="687a0-107">Syntax</span></span>

<span data-ttu-id="687a0-108">DISTTOPATH (\* \* *sección* \* \*, \* \* *x* \* \*, \* \* *y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="687a0-108">DISTTOPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="687a0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="687a0-109">Parameters</span></span>

|<span data-ttu-id="687a0-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="687a0-110">**Name**</span></span>|<span data-ttu-id="687a0-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="687a0-111">**Required/Optional**</span></span>|<span data-ttu-id="687a0-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="687a0-112">**Data Type**</span></span>|<span data-ttu-id="687a0-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="687a0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="687a0-114">_section_</span><span class="sxs-lookup"><span data-stu-id="687a0-114">_section_</span></span> <br/> |<span data-ttu-id="687a0-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="687a0-115">Required</span></span>  <br/> |<span data-ttu-id="687a0-116">**String**</span><span class="sxs-lookup"><span data-stu-id="687a0-116">**String**</span></span> <br/> |<span data-ttu-id="687a0-117">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="687a0-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="687a0-118">_x_</span><span class="sxs-lookup"><span data-stu-id="687a0-118">_x_</span></span> <br/> |<span data-ttu-id="687a0-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="687a0-119">Required</span></span>  <br/> |<span data-ttu-id="687a0-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="687a0-120">**Double**</span></span> <br/> |<span data-ttu-id="687a0-121">Coordenada _x_del punto.</span><span class="sxs-lookup"><span data-stu-id="687a0-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="687a0-122">_y_</span><span class="sxs-lookup"><span data-stu-id="687a0-122">_y_</span></span> <br/> |<span data-ttu-id="687a0-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="687a0-123">Required</span></span>  <br/> |<span data-ttu-id="687a0-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="687a0-124">**Double**</span></span> <br/> |<span data-ttu-id="687a0-125">Coordenada _y_del punto.</span><span class="sxs-lookup"><span data-stu-id="687a0-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="687a0-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="687a0-126">Return value</span></span>

 <span data-ttu-id="687a0-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="687a0-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="687a0-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="687a0-128">Remarks</span></span>

<span data-ttu-id="687a0-129">Microsoft Visio devuelve #REF!</span><span class="sxs-lookup"><span data-stu-id="687a0-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="687a0-130">Si no existe la _sección_ .</span><span class="sxs-lookup"><span data-stu-id="687a0-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="687a0-131">El valor devuelto es positivo si el punto se encuentra a la izquierda de la dirección del recorrido y negativo si se encuentra a la derecha.</span><span class="sxs-lookup"><span data-stu-id="687a0-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

