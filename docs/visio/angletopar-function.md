---
title: ANGLETOPAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
localization_priority: Normal
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: Devuelve un ángulo transformado en el sistema de coordenadas principales de la forma de destino. Convierte las coordenadas locales de un ángulo en una forma de origen a las coordenadas originales en una forma de destino.
ms.openlocfilehash: 3a739c55d568dc548f8175b56f22e6ec4c28e4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821539"
---
# <a name="angletopar-function"></a><span data-ttu-id="82211-104">Función ANGLETOPAR</span><span class="sxs-lookup"><span data-stu-id="82211-104">ANGLETOPAR Function</span></span>

<span data-ttu-id="82211-p102">Devuelve un ángulo transformado en el sistema de coordenadas principales de la forma de destino. Convierte las coordenadas locales de un ángulo en una forma de origen a las coordenadas originales en una forma de destino.
    
</span><span class="sxs-lookup"><span data-stu-id="82211-p102">Returns a transformed angle in the destination shape's parent coordinate system. Converts an angle from local coordinates in a source shape to the parent coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="82211-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82211-107">Syntax</span></span>

<span data-ttu-id="82211-108">ANGLETOPAR (** *ánguloOrigen* **, ** *refOrigen* **, ** *refDestino* **)</span><span class="sxs-lookup"><span data-stu-id="82211-108">ANGLETOPAR(** *srcAngle* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="82211-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82211-109">Parameters</span></span>

|<span data-ttu-id="82211-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="82211-110">**Name**</span></span>|<span data-ttu-id="82211-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="82211-111">**Required/Optional**</span></span>|<span data-ttu-id="82211-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="82211-112">**Data Type**</span></span>|<span data-ttu-id="82211-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82211-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="82211-114">_ánguloOrigen_</span><span class="sxs-lookup"><span data-stu-id="82211-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="82211-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="82211-115">Required</span></span>  <br/> |<span data-ttu-id="82211-116">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="82211-116">**Numeric**</span></span> <br/> |<span data-ttu-id="82211-117">Un ángulo en el sistema de coordenadas de origen.</span><span class="sxs-lookup"><span data-stu-id="82211-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="82211-118">_refOrigen_</span><span class="sxs-lookup"><span data-stu-id="82211-118">_srcRef_</span></span> <br/> |<span data-ttu-id="82211-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="82211-119">Required</span></span>  <br/> |<span data-ttu-id="82211-120">**String**</span><span class="sxs-lookup"><span data-stu-id="82211-120">**String**</span></span> <br/> | <span data-ttu-id="82211-121">Una referencia a una celda en el objeto de origen, como una forma, grupo, página, etcétera.</span><span class="sxs-lookup"><span data-stu-id="82211-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="82211-122">_refDestino_</span><span class="sxs-lookup"><span data-stu-id="82211-122">_dstRef_</span></span> <br/> |<span data-ttu-id="82211-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="82211-123">Required</span></span>  <br/> |<span data-ttu-id="82211-124">**String**</span><span class="sxs-lookup"><span data-stu-id="82211-124">**String**</span></span> <br/> |<span data-ttu-id="82211-125">Una referencia a una celda en el objeto de destino, como una forma, grupo, página, etcétera.</span><span class="sxs-lookup"><span data-stu-id="82211-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82211-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82211-126">Remarks</span></span>

<span data-ttu-id="82211-p103">Esta función sirve incluso en el caso de que las formas de origen y de destino formen parte de grupos. También ajusta el giro y el volteo en la transformación intermedia.</span><span class="sxs-lookup"><span data-stu-id="82211-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="82211-129">Las coordenadas de origen y de destino deben encontrarse en la misma página.</span><span class="sxs-lookup"><span data-stu-id="82211-129">The source and destination coordinates must be on the same page.</span></span>
  
<span data-ttu-id="82211-130">Si el destino es una página que carece de forma principal, el resultado se expresará en las coordenadas locales de la página.</span><span class="sxs-lookup"><span data-stu-id="82211-130">If the destination is a page, which has no parent, the result is expressed in page's local coordinates.</span></span>
  

