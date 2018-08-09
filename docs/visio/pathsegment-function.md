---
title: PATHSEGMENT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Devuelve el número de segmento basado en 1 en la marca de porcentaje especificado a lo largo de la ruta de acceso especificada.
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822740"
---
# <a name="pathsegment-function"></a><span data-ttu-id="77771-103">Función PATHSEGMENT</span><span class="sxs-lookup"><span data-stu-id="77771-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="77771-104">Devuelve el número de segmento basado en 1 en la marca de porcentaje especificado a lo largo de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="77771-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="77771-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77771-105">Syntax</span></span>

<span data-ttu-id="77771-106">PATHSEGMENT (** *sección* **, ** *viajes* **)</span><span class="sxs-lookup"><span data-stu-id="77771-106">PATHSEGMENT(** *section* **, ** *travel* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="77771-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77771-107">Parameters</span></span>

|<span data-ttu-id="77771-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="77771-108">**Name**</span></span>|<span data-ttu-id="77771-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="77771-109">**Required/Optional**</span></span>|<span data-ttu-id="77771-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="77771-110">**Data Type**</span></span>|<span data-ttu-id="77771-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77771-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="77771-112">_section_</span><span class="sxs-lookup"><span data-stu-id="77771-112">_section_</span></span> <br/> |<span data-ttu-id="77771-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="77771-113">Required</span></span>  <br/> |<span data-ttu-id="77771-114">**String**</span><span class="sxs-lookup"><span data-stu-id="77771-114">**String**</span></span> <br/> |<span data-ttu-id="77771-115">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="77771-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="77771-116">_viajes_</span><span class="sxs-lookup"><span data-stu-id="77771-116">_travel_</span></span> <br/> |<span data-ttu-id="77771-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="77771-117">Required</span></span>  <br/> |<span data-ttu-id="77771-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="77771-118">**Double**</span></span> <br/> |<span data-ttu-id="77771-p101">Porcentaje de la ruta de acceso atravesado, desde el punto inicial al punto final. Debe oscilar entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="77771-p101">The percentage of the path traversed, from the begin point to the end point. Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="77771-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77771-121">Return value</span></span>

<span data-ttu-id="77771-122">Entero</span><span class="sxs-lookup"><span data-stu-id="77771-122">Integer</span></span>
  

