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
ms.openlocfilehash: 0fed51e264bfb21da25d4e91f20f4bc0803e46e8
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160261"
---
# <a name="angletopar-function"></a><span data-ttu-id="06f67-104">Función ANGLETOPAR</span><span class="sxs-lookup"><span data-stu-id="06f67-104">ANGLETOPAR Function</span></span>

<span data-ttu-id="06f67-105">Devuelve un ángulo transformado en el sistema de coordenadas principales de la forma de destino.</span><span class="sxs-lookup"><span data-stu-id="06f67-105">Returns a transformed angle in the destination shape's parent coordinate system.</span></span> <span data-ttu-id="06f67-106">Convierte las coordenadas locales de un ángulo en una forma de origen a las coordenadas originales en una forma de destino.</span><span class="sxs-lookup"><span data-stu-id="06f67-106">Converts an angle from local coordinates in a source shape to the parent coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="06f67-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06f67-107">Syntax</span></span>

<span data-ttu-id="06f67-108">ANGLETOPAR (***srcAngle***, ***srcRef***, ***dstRef*** )</span><span class="sxs-lookup"><span data-stu-id="06f67-108">ANGLETOPAR(***srcAngle***, ***srcRef***, ***dstRef*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="06f67-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06f67-109">Parameters</span></span>

|<span data-ttu-id="06f67-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="06f67-110">**Name**</span></span>|<span data-ttu-id="06f67-111">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="06f67-111">**Required/Optional**</span></span>|<span data-ttu-id="06f67-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="06f67-112">**Data Type**</span></span>|<span data-ttu-id="06f67-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06f67-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="06f67-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="06f67-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="06f67-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06f67-115">Required</span></span>  <br/> |<span data-ttu-id="06f67-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="06f67-116">**Numeric**</span></span> <br/> |<span data-ttu-id="06f67-117">Un ángulo en el sistema de coordenadas de origen.</span><span class="sxs-lookup"><span data-stu-id="06f67-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="06f67-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="06f67-118">_srcRef_</span></span> <br/> |<span data-ttu-id="06f67-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06f67-119">Required</span></span>  <br/> |<span data-ttu-id="06f67-120">**String**</span><span class="sxs-lookup"><span data-stu-id="06f67-120">**String**</span></span> <br/> | <span data-ttu-id="06f67-121">Una referencia a una celda en el objeto de origen, como una forma, grupo, página, etcétera.</span><span class="sxs-lookup"><span data-stu-id="06f67-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="06f67-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="06f67-122">_dstRef_</span></span> <br/> |<span data-ttu-id="06f67-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="06f67-123">Required</span></span>  <br/> |<span data-ttu-id="06f67-124">**String**</span><span class="sxs-lookup"><span data-stu-id="06f67-124">**String**</span></span> <br/> |<span data-ttu-id="06f67-125">Una referencia a una celda en el objeto de destino, como una forma, grupo, página, etcétera.</span><span class="sxs-lookup"><span data-stu-id="06f67-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06f67-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06f67-126">Remarks</span></span>

<span data-ttu-id="06f67-p103">Esta función sirve incluso en el caso de que las formas de origen y de destino formen parte de grupos. También ajusta el giro y el volteo en la transformación intermedia.</span><span class="sxs-lookup"><span data-stu-id="06f67-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="06f67-129">Las coordenadas de origen y de destino deben encontrarse en la misma página.</span><span class="sxs-lookup"><span data-stu-id="06f67-129">The source and destination coordinates must be on the same page.</span></span>
  
<span data-ttu-id="06f67-130">Si el destino es una página que carece de forma principal, el resultado se expresará en las coordenadas locales de la página.</span><span class="sxs-lookup"><span data-stu-id="06f67-130">If the destination is a page, which has no parent, the result is expressed in page's local coordinates.</span></span>
  

