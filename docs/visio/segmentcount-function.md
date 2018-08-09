---
title: SEGMENTCOUNT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Devuelve el número de segmentos de línea que conforma la ruta de acceso.
ms.openlocfilehash: 93a77d9085e6900f502a75401847ad685d25effd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823130"
---
# <a name="segmentcount-function"></a><span data-ttu-id="50665-103">Función SEGMENTCOUNT</span><span class="sxs-lookup"><span data-stu-id="50665-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="50665-104">Devuelve el número de segmentos de línea que conforma la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="50665-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="50665-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50665-105">Syntax</span></span>

<span data-ttu-id="50665-106">SEGMENTCOUNT (** *pathRef* **)</span><span class="sxs-lookup"><span data-stu-id="50665-106">SEGMENTCOUNT(** *pathRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="50665-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50665-107">Parameters</span></span>

|<span data-ttu-id="50665-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="50665-108">**Name**</span></span>|<span data-ttu-id="50665-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="50665-109">**Required/Optional**</span></span>|<span data-ttu-id="50665-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="50665-110">**Data Type**</span></span>|<span data-ttu-id="50665-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="50665-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="50665-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="50665-112">_pathRef_</span></span> <br/> |<span data-ttu-id="50665-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="50665-113">Required</span></span>  <br/> |<span data-ttu-id="50665-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="50665-114">**Integer**</span></span> <br/> |<span data-ttu-id="50665-115">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="50665-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="50665-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50665-116">Return value</span></span>

<span data-ttu-id="50665-117">Entero</span><span class="sxs-lookup"><span data-stu-id="50665-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50665-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50665-118">Remarks</span></span>

<span data-ttu-id="50665-119">Los saltos de línea no se incluyen en el número total de segmentos devuelto.</span><span class="sxs-lookup"><span data-stu-id="50665-119">Line jumps are not included in the total number of segments returned.</span></span>
  

