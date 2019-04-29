---
title: PATHSEGMENT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Devuelve el número de segmento basado en 1 en la marca de porcentaje especificada a lo largo de la ruta de acceso especificada.
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432488"
---
# <a name="pathsegment-function"></a><span data-ttu-id="05879-103">Función PATHSEGMENT</span><span class="sxs-lookup"><span data-stu-id="05879-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="05879-104">Devuelve el número de segmento basado en 1 en la marca de porcentaje especificada a lo largo de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="05879-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="05879-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05879-105">Syntax</span></span>

<span data-ttu-id="05879-106">PATHSEGMENT (\* \* *sección* \* \*, \* \* *viaje* \* \*)</span><span class="sxs-lookup"><span data-stu-id="05879-106">PATHSEGMENT(\*\* *section* \*\*, \*\* *travel* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="05879-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05879-107">Parameters</span></span>

|<span data-ttu-id="05879-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="05879-108">**Name**</span></span>|<span data-ttu-id="05879-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="05879-109">**Required/Optional**</span></span>|<span data-ttu-id="05879-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="05879-110">**Data Type**</span></span>|<span data-ttu-id="05879-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05879-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="05879-112">_section_</span><span class="sxs-lookup"><span data-stu-id="05879-112">_section_</span></span> <br/> |<span data-ttu-id="05879-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="05879-113">Required</span></span>  <br/> |<span data-ttu-id="05879-114">**String**</span><span class="sxs-lookup"><span data-stu-id="05879-114">**String**</span></span> <br/> |<span data-ttu-id="05879-115">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="05879-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="05879-116">_carrera_</span><span class="sxs-lookup"><span data-stu-id="05879-116">_travel_</span></span> <br/> |<span data-ttu-id="05879-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="05879-117">Required</span></span>  <br/> |<span data-ttu-id="05879-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="05879-118">**Double**</span></span> <br/> |<span data-ttu-id="05879-119">Porcentaje de la ruta de acceso atravesado, desde el punto inicial al punto final.</span><span class="sxs-lookup"><span data-stu-id="05879-119">The percentage of the path traversed, from the begin point to the end point.</span></span> <span data-ttu-id="05879-120">Debe oscilar entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="05879-120">Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="05879-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05879-121">Return value</span></span>

<span data-ttu-id="05879-122">Entero</span><span class="sxs-lookup"><span data-stu-id="05879-122">Integer</span></span>
  

