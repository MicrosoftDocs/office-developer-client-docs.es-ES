---
title: PATHLENGTH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Devuelve la longitud de la ruta de acceso definida en la sección de geometría especificada.
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822735"
---
# <a name="pathlength-function"></a><span data-ttu-id="19ebc-103">Función PATHLENGTH</span><span class="sxs-lookup"><span data-stu-id="19ebc-103">PATHLENGTH Function</span></span>

<span data-ttu-id="19ebc-104">Devuelve la longitud de la ruta de acceso definida en la sección de geometría especificada.</span><span class="sxs-lookup"><span data-stu-id="19ebc-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="19ebc-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="19ebc-105">Version Information</span></span>

<span data-ttu-id="19ebc-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="19ebc-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="19ebc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19ebc-107">Syntax</span></span>

<span data-ttu-id="19ebc-108">PATHLENGTH (** *sección* ** ** *[, segmento]* **)</span><span class="sxs-lookup"><span data-stu-id="19ebc-108">PATHLENGTH(** *section* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="19ebc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19ebc-109">Parameters</span></span>

|<span data-ttu-id="19ebc-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="19ebc-110">**Name**</span></span>|<span data-ttu-id="19ebc-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="19ebc-111">**Required/Optional**</span></span>|<span data-ttu-id="19ebc-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="19ebc-112">**Data Type**</span></span>|<span data-ttu-id="19ebc-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="19ebc-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="19ebc-114">_section_</span><span class="sxs-lookup"><span data-stu-id="19ebc-114">_section_</span></span> <br/> |<span data-ttu-id="19ebc-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="19ebc-115">Required</span></span>  <br/> |<span data-ttu-id="19ebc-116">**String**</span><span class="sxs-lookup"><span data-stu-id="19ebc-116">**String**</span></span> <br/> |<span data-ttu-id="19ebc-117">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="19ebc-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="19ebc-118">_segmento_</span><span class="sxs-lookup"><span data-stu-id="19ebc-118">_segment_</span></span> <br/> |<span data-ttu-id="19ebc-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="19ebc-119">Optional</span></span>  <br/> |<span data-ttu-id="19ebc-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="19ebc-120">**Integer**</span></span> <br/> |<span data-ttu-id="19ebc-121">Segmento basado en 1 de la ruta de acceso que se va a medir.</span><span class="sxs-lookup"><span data-stu-id="19ebc-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="19ebc-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19ebc-122">Return value</span></span>

 <span data-ttu-id="19ebc-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="19ebc-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19ebc-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="19ebc-124">Remarks</span></span>

<span data-ttu-id="19ebc-125">Si no existe _section_ ni _segment_ , Microsoft Visio devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="19ebc-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="19ebc-126">Si incluye un valor _segment_ , PATHLENGTH devuelve la longitud de ese segmento solo.</span><span class="sxs-lookup"><span data-stu-id="19ebc-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

