---
title: LOCTOLOC (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
localization_priority: Normal
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: Devuelve un punto transformado en las coordenadas locales en el sistema de coordenadas de destino.
ms.openlocfilehash: 444200801ebd984fb735b95de6d58d35e5160d1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822558"
---
# <a name="loctoloc-function"></a><span data-ttu-id="156e7-103">Función LOCTOLOC</span><span class="sxs-lookup"><span data-stu-id="156e7-103">LOCTOLOC Function</span></span>

<span data-ttu-id="156e7-104">Devuelve un punto transformado en las coordenadas locales en el sistema de coordenadas de destino.</span><span class="sxs-lookup"><span data-stu-id="156e7-104">Returns a transformed point in local coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="156e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="156e7-105">Syntax</span></span>

<span data-ttu-id="156e7-106">LOCTOLOC (** *puntoOrigen* **, ** *refOrigen* **, ** *refDestino* **)</span><span class="sxs-lookup"><span data-stu-id="156e7-106">LOCTOLOC(** *srcPoint* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="156e7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="156e7-107">Parameters</span></span>

|<span data-ttu-id="156e7-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="156e7-108">**Name**</span></span>|<span data-ttu-id="156e7-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="156e7-109">**Required/Optional**</span></span>|<span data-ttu-id="156e7-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="156e7-110">**Data Type**</span></span>|<span data-ttu-id="156e7-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="156e7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="156e7-112">_puntoOrigen_</span><span class="sxs-lookup"><span data-stu-id="156e7-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="156e7-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="156e7-113">Required</span></span>  <br/> |<span data-ttu-id="156e7-114">**String**</span><span class="sxs-lookup"><span data-stu-id="156e7-114">**String**</span></span> <br/> | <span data-ttu-id="156e7-115">Punto del sistema de coordenadas de origen, en las coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="156e7-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="156e7-116">_refOrigen_</span><span class="sxs-lookup"><span data-stu-id="156e7-116">_srcRef_</span></span> <br/> |<span data-ttu-id="156e7-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="156e7-117">Required</span></span>  <br/> |<span data-ttu-id="156e7-118">**String**</span><span class="sxs-lookup"><span data-stu-id="156e7-118">**String**</span></span> <br/> | <span data-ttu-id="156e7-119">Referencia a una celda en el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="156e7-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="156e7-120">_refDestino_</span><span class="sxs-lookup"><span data-stu-id="156e7-120">_dstRef_</span></span> <br/> |<span data-ttu-id="156e7-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="156e7-121">Required</span></span>  <br/> |<span data-ttu-id="156e7-122">**String**</span><span class="sxs-lookup"><span data-stu-id="156e7-122">**String**</span></span> <br/> | <span data-ttu-id="156e7-123">Referencia a una celda en el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="156e7-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="156e7-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="156e7-124">Return value</span></span>

<span data-ttu-id="156e7-125">String</span><span class="sxs-lookup"><span data-stu-id="156e7-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="156e7-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="156e7-126">Remarks</span></span>

<span data-ttu-id="156e7-p101">La función LOCTOLOC convierte las coordenadas locales de un punto en una forma de origen a las coordenadas locales en una forma de destino. Puede utilizar esta función para construir una forma, por ejemplo, usando como referencia un punto de otro espacio de coordenadas distinto. También puede utilizar esta función para convertir un punto local en sus coordenadas de página o viceversa.</span><span class="sxs-lookup"><span data-stu-id="156e7-p101">The LOCTOLOC function converts a point from local coordinates in a source shape to local coordinates in a destination shape. You can use this function to construct a shape, for example, in terms of a point from another coordinate space. You can also use this function to transform a local point to page coordinates, or vice versa.</span></span>
  
<span data-ttu-id="156e7-p102">Esta función sirve incluso en el caso de que las formas de origen y de destino formen parte de grupos. También ajusta el giro y el volteo en la transformación intermedia.</span><span class="sxs-lookup"><span data-stu-id="156e7-p102">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="156e7-132">Las coordenadas de origen y de destino deben encontrarse en la misma página.</span><span class="sxs-lookup"><span data-stu-id="156e7-132">The source and destination coordinates must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="156e7-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="156e7-133">Example</span></span>

<span data-ttu-id="156e7-134">La siguiente fórmula convierte el eje local de la forma asociada con la fórmula en un punto de la página.</span><span class="sxs-lookup"><span data-stu-id="156e7-134">The following formula converts the local pin of the shape associated with the formula to a point on the page.</span></span>
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


