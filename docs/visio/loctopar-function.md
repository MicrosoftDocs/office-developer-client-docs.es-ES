---
title: LOCTOPAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: Devuelve un punto transformado en las coordenadas principales en el sistema de coordenadas de destino.
ms.openlocfilehash: 7d882ec34de93db2828fc751f99d87fc3e961d64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822567"
---
# <a name="loctopar-function"></a><span data-ttu-id="fe51a-103">Función LOCTOPAR</span><span class="sxs-lookup"><span data-stu-id="fe51a-103">LOCTOPAR Function</span></span>

<span data-ttu-id="fe51a-104">Devuelve un punto transformado en las coordenadas principales en el sistema de coordenadas de destino.</span><span class="sxs-lookup"><span data-stu-id="fe51a-104">Returns a transformed point in parent coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fe51a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe51a-105">Syntax</span></span>

<span data-ttu-id="fe51a-106">LOCTOPAR (** *puntoOrigen* **, ** *refOrigen* **, ** *refDestino* **)</span><span class="sxs-lookup"><span data-stu-id="fe51a-106">LOCTOPAR(** *srcPoint* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fe51a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe51a-107">Parameters</span></span>

|<span data-ttu-id="fe51a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fe51a-108">**Name**</span></span>|<span data-ttu-id="fe51a-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="fe51a-109">**Required/Optional**</span></span>|<span data-ttu-id="fe51a-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="fe51a-110">**Data Type**</span></span>|<span data-ttu-id="fe51a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fe51a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fe51a-112">_puntoOrigen_</span><span class="sxs-lookup"><span data-stu-id="fe51a-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="fe51a-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fe51a-113">Required</span></span>  <br/> |<span data-ttu-id="fe51a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fe51a-114">**String**</span></span> <br/> | <span data-ttu-id="fe51a-115">Punto del sistema de coordenadas de origen, en las coordenadas locales.</span><span class="sxs-lookup"><span data-stu-id="fe51a-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="fe51a-116">_refOrigen_</span><span class="sxs-lookup"><span data-stu-id="fe51a-116">_srcRef_</span></span> <br/> |<span data-ttu-id="fe51a-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fe51a-117">Required</span></span>  <br/> |<span data-ttu-id="fe51a-118">**String**</span><span class="sxs-lookup"><span data-stu-id="fe51a-118">**String**</span></span> <br/> | <span data-ttu-id="fe51a-119">Referencia a una celda en el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="fe51a-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="fe51a-120">_refDestino_</span><span class="sxs-lookup"><span data-stu-id="fe51a-120">_dstRef_</span></span> <br/> |<span data-ttu-id="fe51a-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fe51a-121">Required</span></span>  <br/> |<span data-ttu-id="fe51a-122">**String**</span><span class="sxs-lookup"><span data-stu-id="fe51a-122">**String**</span></span> <br/> | <span data-ttu-id="fe51a-123">Referencia a una celda en el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="fe51a-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fe51a-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe51a-124">Return value</span></span>

<span data-ttu-id="fe51a-125">String</span><span class="sxs-lookup"><span data-stu-id="fe51a-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe51a-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe51a-126">Remarks</span></span>

<span data-ttu-id="fe51a-p101">Convierte las coordenadas locales de un punto en una forma de origen a las coordenadas principales en una forma de destino. Puede utilizar la función LOCTOPAR para establecer coordenadas principales en las celdas, como PinX, PinY, BeginX y BeginY en una forma utilizando otro punto de un sistema de coordenadas distinto.</span><span class="sxs-lookup"><span data-stu-id="fe51a-p101">Converts a point from local coordinates in a source shape to parent coordinates in a destination shape. You can use the LOCTOPAR function to set parent coordinates in cells, such as PinX, PinY, BeginX, and BeginY in a shape using another point from another coordinate system.</span></span> 
  
<span data-ttu-id="fe51a-p102">Esta función sirve incluso en el caso de que las formas de origen y de destino formen parte de grupos. También ajusta el giro y el volteo en la transformación intermedia.</span><span class="sxs-lookup"><span data-stu-id="fe51a-p102">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span> 
  
<span data-ttu-id="fe51a-131">Las coordenadas de origen y de destino deben encontrarse en la misma página.</span><span class="sxs-lookup"><span data-stu-id="fe51a-131">The source and destination coordinates must be on the same page.</span></span> 
  
<span data-ttu-id="fe51a-132">Si el destino es una página que carece de forma principal, el resultado se expresará en las coordenadas locales de la página.</span><span class="sxs-lookup"><span data-stu-id="fe51a-132">If the destination is a page, which has no parent, the result is expressed in the page's local coordinates.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fe51a-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe51a-133">Example</span></span>

<span data-ttu-id="fe51a-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width, Hoja.4!Width)</span><span class="sxs-lookup"><span data-stu-id="fe51a-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width)</span></span> 
  
<span data-ttu-id="fe51a-135">Convierte el eje local de la forma asociada con la fórmula a las coordenadas principales de la Hoja.4.</span><span class="sxs-lookup"><span data-stu-id="fe51a-135">Converts the local pin of the shape associated with the formula to parent coordinates of Sheet.4.</span></span> 
  

