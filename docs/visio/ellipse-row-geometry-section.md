---
title: Fila Ellipse (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Contiene las coordenadas x e y del punto central y de dos puntos de la elipse.
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421833"
---
# <a name="ellipse-row-geometry-section"></a><span data-ttu-id="f7809-103">Fila Ellipse (Sección de Geometría)</span><span class="sxs-lookup"><span data-stu-id="f7809-103">Ellipse Row (Geometry Section)</span></span>

<span data-ttu-id="f7809-104">Contiene las coordenadas *x* e \*\* y del punto central y de dos puntos de la elipse.</span><span class="sxs-lookup"><span data-stu-id="f7809-104">Contains the  *x*  - and  *y*  -coordinates of the ellipse's center point and two points on the ellipse.</span></span> 
  
<span data-ttu-id="f7809-105">Las filas Ellipse contienen las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f7809-105">An Ellipse row contains the following cells.</span></span>
  
|<span data-ttu-id="f7809-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="f7809-106">**Cell**</span></span>|<span data-ttu-id="f7809-107">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f7809-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7809-108">X</span><span class="sxs-lookup"><span data-stu-id="f7809-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="f7809-109">Coordenada *x* del punto central.</span><span class="sxs-lookup"><span data-stu-id="f7809-109">The  *x*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="f7809-110">Y</span><span class="sxs-lookup"><span data-stu-id="f7809-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="f7809-111">Coordenada *y* del punto central.</span><span class="sxs-lookup"><span data-stu-id="f7809-111">The  *y*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="f7809-112">A</span><span class="sxs-lookup"><span data-stu-id="f7809-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="f7809-113">Coordenada x de un punto de la elipse; emparejado con la coordenada *y* representada por la celda B.</span><span class="sxs-lookup"><span data-stu-id="f7809-113">The x-coordinate of one point on the ellipse; paired with  *y*  -coordinate represented by the B cell.</span></span>  <br/> |
|[<span data-ttu-id="f7809-114">B</span><span class="sxs-lookup"><span data-stu-id="f7809-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="f7809-115">Coordenada *y* de un punto de la elipse; emparejado con la coordenada x representada por la celda A.</span><span class="sxs-lookup"><span data-stu-id="f7809-115">The  *y*  -coordinate of one point on the ellipse; paired with x-coordinate represented by the A cell.</span></span>  <br/> |
|[<span data-ttu-id="f7809-116">CA</span><span class="sxs-lookup"><span data-stu-id="f7809-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="f7809-117">Coordenada *x* de otro punto de la elipse; emparejado con la coordenada *y* representada por la celda D.</span><span class="sxs-lookup"><span data-stu-id="f7809-117">The  *x*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the D cell.</span></span>  <br/> |
|[<span data-ttu-id="f7809-118">D</span><span class="sxs-lookup"><span data-stu-id="f7809-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="f7809-119">Coordenada *y* de otro punto de la elipse; emparejado con la coordenada *y* representada por la celda C.</span><span class="sxs-lookup"><span data-stu-id="f7809-119">The  *y*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the C cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7809-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7809-120">Remarks</span></span>

<span data-ttu-id="f7809-121">Una sección de geometría que contenga una fila Ellipse o InfiniteLine no debe contener otras filas.</span><span class="sxs-lookup"><span data-stu-id="f7809-121">A geometry section that contains an Ellipse or an InfiniteLine row should not contain any other rows.</span></span>
  

