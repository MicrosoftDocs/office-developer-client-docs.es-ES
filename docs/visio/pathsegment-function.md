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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344453"
---
# <a name="pathsegment-function"></a><span data-ttu-id="54bec-103">Función PATHSEGMENT</span><span class="sxs-lookup"><span data-stu-id="54bec-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="54bec-104">Devuelve el número de segmento basado en 1 en la marca de porcentaje especificada a lo largo de la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="54bec-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="54bec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54bec-105">Syntax</span></span>

<span data-ttu-id="54bec-106">PATHSEGMENT (\* \* *sección* \* \*, \* \* *viaje* \* \*)</span><span class="sxs-lookup"><span data-stu-id="54bec-106">PATHSEGMENT(\*\* *section* \*\*, \*\* *travel* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="54bec-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54bec-107">Parameters</span></span>

|<span data-ttu-id="54bec-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="54bec-108">**Name**</span></span>|<span data-ttu-id="54bec-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="54bec-109">**Required/Optional**</span></span>|<span data-ttu-id="54bec-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="54bec-110">**Data Type**</span></span>|<span data-ttu-id="54bec-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="54bec-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="54bec-112">_section_</span><span class="sxs-lookup"><span data-stu-id="54bec-112">_section_</span></span> <br/> |<span data-ttu-id="54bec-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="54bec-113">Required</span></span>  <br/> |<span data-ttu-id="54bec-114">**String**</span><span class="sxs-lookup"><span data-stu-id="54bec-114">**String**</span></span> <br/> |<span data-ttu-id="54bec-115">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="54bec-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="54bec-116">_carrera_</span><span class="sxs-lookup"><span data-stu-id="54bec-116">_travel_</span></span> <br/> |<span data-ttu-id="54bec-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="54bec-117">Required</span></span>  <br/> |<span data-ttu-id="54bec-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="54bec-118">**Double**</span></span> <br/> |<span data-ttu-id="54bec-119">Porcentaje de la ruta de acceso atravesado, desde el punto inicial al punto final.</span><span class="sxs-lookup"><span data-stu-id="54bec-119">The percentage of the path traversed, from the begin point to the end point.</span></span> <span data-ttu-id="54bec-120">Debe oscilar entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="54bec-120">Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="54bec-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54bec-121">Return value</span></span>

<span data-ttu-id="54bec-122">Entero</span><span class="sxs-lookup"><span data-stu-id="54bec-122">Integer</span></span>
  

