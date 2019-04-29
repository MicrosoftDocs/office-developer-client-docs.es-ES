---
title: ANGLETOLOC (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
localization_priority: Normal
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: Devuelve un ángulo transformado en el sistema de coordenadas local de la forma de destino. Convierte las coordenadas locales de un ángulo en una forma de origen a las coordenadas locales en una forma de destino.
ms.openlocfilehash: 804faeb24932e414ad03bc9e8487c62ca08bd7d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433573"
---
# <a name="angletoloc-function"></a><span data-ttu-id="292e9-104">Función ANGLETOLOC</span><span class="sxs-lookup"><span data-stu-id="292e9-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="292e9-105">Devuelve un ángulo transformado en el sistema de coordenadas local de la forma de destino.</span><span class="sxs-lookup"><span data-stu-id="292e9-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="292e9-106">Convierte las coordenadas locales de un ángulo en una forma de origen a las coordenadas locales en una forma de destino.</span><span class="sxs-lookup"><span data-stu-id="292e9-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="292e9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="292e9-107">Syntax</span></span>

<span data-ttu-id="292e9-108">ANGLETOLOC (\* \* *srcAngle* \* \*, \* \* *srcRef* \* \*, \* \* *dstRef* \* \*)</span><span class="sxs-lookup"><span data-stu-id="292e9-108">ANGLETOLOC(\*\* *srcAngle* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="292e9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="292e9-109">Parameters</span></span>

|<span data-ttu-id="292e9-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="292e9-110">**Name**</span></span>|<span data-ttu-id="292e9-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="292e9-111">**Required/Optional**</span></span>|<span data-ttu-id="292e9-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="292e9-112">**Data Type**</span></span>|<span data-ttu-id="292e9-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="292e9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="292e9-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="292e9-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="292e9-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="292e9-115">Required</span></span>  <br/> |<span data-ttu-id="292e9-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="292e9-116">**Numeric**</span></span> <br/> |<span data-ttu-id="292e9-117">Un ángulo en el sistema de coordenadas de origen.</span><span class="sxs-lookup"><span data-stu-id="292e9-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="292e9-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="292e9-118">_srcRef_</span></span> <br/> |<span data-ttu-id="292e9-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="292e9-119">Required</span></span>  <br/> |<span data-ttu-id="292e9-120">**String**</span><span class="sxs-lookup"><span data-stu-id="292e9-120">**String**</span></span> <br/> | <span data-ttu-id="292e9-121">Una referencia a una celda en el objeto de origen, como una forma, grupo, página, etcétera.</span><span class="sxs-lookup"><span data-stu-id="292e9-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="292e9-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="292e9-122">_dstRef_</span></span> <br/> |<span data-ttu-id="292e9-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="292e9-123">Required</span></span>  <br/> |<span data-ttu-id="292e9-124">**String**</span><span class="sxs-lookup"><span data-stu-id="292e9-124">**String**</span></span> <br/> |<span data-ttu-id="292e9-125">Una referencia a una celda en el objeto de destino, como una forma, grupo, página, etcétera.</span><span class="sxs-lookup"><span data-stu-id="292e9-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="292e9-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="292e9-126">Remarks</span></span>

<span data-ttu-id="292e9-127">Puede usar la función ÁNGULOALOC para establecer celdas de ángulo local en una forma en términos de un ángulo desde otro espacio de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="292e9-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="292e9-p103">Esta función sirve incluso en el caso de que las formas de origen y de destino formen parte de grupos. También ajusta el giro y el volteo en la transformación intermedia.</span><span class="sxs-lookup"><span data-stu-id="292e9-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="292e9-130">Las coordenadas de origen y de destino deben encontrarse en la misma página.</span><span class="sxs-lookup"><span data-stu-id="292e9-130">The source and destination coordinates must be on the same page.</span></span>
  

