---
title: PATHLENGTH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Devuelve la longitud de la ruta de acceso definida en la sección de geometría especificada.
ms.openlocfilehash: e4f90c2bb886f54164bedab5f8d78fc528758414
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405852"
---
# <a name="pathlength-function"></a><span data-ttu-id="31587-103">Función PATHLENGTH</span><span class="sxs-lookup"><span data-stu-id="31587-103">PATHLENGTH Function</span></span>

<span data-ttu-id="31587-104">Devuelve la longitud de la ruta de acceso definida en la sección de geometría especificada.</span><span class="sxs-lookup"><span data-stu-id="31587-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="31587-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="31587-105">Version Information</span></span>

<span data-ttu-id="31587-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="31587-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="31587-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31587-107">Syntax</span></span>

<span data-ttu-id="31587-108">PATHLENGTH(\*\* *section* \*\* *[,segment]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="31587-108">PATHLENGTH(\*\* *section* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="31587-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31587-109">Parameters</span></span>

|<span data-ttu-id="31587-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="31587-110">**Name**</span></span>|<span data-ttu-id="31587-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="31587-111">**Required/Optional**</span></span>|<span data-ttu-id="31587-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="31587-112">**Data Type**</span></span>|<span data-ttu-id="31587-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31587-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="31587-114">_section_</span><span class="sxs-lookup"><span data-stu-id="31587-114">_section_</span></span> <br/> |<span data-ttu-id="31587-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="31587-115">Required</span></span>  <br/> |<span data-ttu-id="31587-116">**String**</span><span class="sxs-lookup"><span data-stu-id="31587-116">**String**</span></span> <br/> |<span data-ttu-id="31587-117">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="31587-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="31587-118">_segmentos_</span><span class="sxs-lookup"><span data-stu-id="31587-118">_segment_</span></span> <br/> |<span data-ttu-id="31587-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="31587-119">Optional</span></span>  <br/> |<span data-ttu-id="31587-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="31587-120">**Integer**</span></span> <br/> |<span data-ttu-id="31587-121">Segmento basado en 1 de la ruta de acceso que se va a medir.</span><span class="sxs-lookup"><span data-stu-id="31587-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="31587-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31587-122">Return value</span></span>

 <span data-ttu-id="31587-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="31587-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31587-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31587-124">Remarks</span></span>

<span data-ttu-id="31587-125">Si  _la_ sección  _o el segmento_ no existen, Microsoft Visio devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="31587-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="31587-126">Si incluyes un  _valor de_ segmento, PATHLENGTH solo devuelve la longitud de ese segmento.</span><span class="sxs-lookup"><span data-stu-id="31587-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

