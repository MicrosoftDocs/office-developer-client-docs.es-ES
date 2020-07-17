---
title: RECTSECT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
localization_priority: Normal
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: Calcula el sector de un rectángulo asociado con x e y y devuelve un entero de 0 a 4, que indica el sector.
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160275"
---
# <a name="rectsect-function"></a><span data-ttu-id="9ce37-103">Función RECTSECT</span><span class="sxs-lookup"><span data-stu-id="9ce37-103">RECTSECT Function</span></span>

<span data-ttu-id="9ce37-104">Calcula el sector de un rectángulo asociado con *x* e y *y devuelve* un entero de 0 a 4, que indica el sector.</span><span class="sxs-lookup"><span data-stu-id="9ce37-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9ce37-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ce37-105">Syntax</span></span>

<span data-ttu-id="9ce37-106">RECTSECT (***width***, ***height***, ***x***, ***y***, ***opción*** )</span><span class="sxs-lookup"><span data-stu-id="9ce37-106">RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9ce37-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ce37-107">Parameters</span></span>

|<span data-ttu-id="9ce37-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9ce37-108">**Name**</span></span>|<span data-ttu-id="9ce37-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="9ce37-109">**Required/Optional**</span></span>|<span data-ttu-id="9ce37-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="9ce37-110">**Data Type**</span></span>|<span data-ttu-id="9ce37-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9ce37-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9ce37-112">_width_</span><span class="sxs-lookup"><span data-stu-id="9ce37-112">_width_</span></span> <br/> |<span data-ttu-id="9ce37-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9ce37-113">Required</span></span>  <br/> |<span data-ttu-id="9ce37-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9ce37-114">**String**</span></span> <br/> |<span data-ttu-id="9ce37-115">El ancho del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="9ce37-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="9ce37-116">_height_</span><span class="sxs-lookup"><span data-stu-id="9ce37-116">_height_</span></span> <br/> |<span data-ttu-id="9ce37-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9ce37-117">Required</span></span>  <br/> |<span data-ttu-id="9ce37-118">**String**</span><span class="sxs-lookup"><span data-stu-id="9ce37-118">**String**</span></span> <br/> |<span data-ttu-id="9ce37-119">El alto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="9ce37-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="9ce37-120">_x_</span><span class="sxs-lookup"><span data-stu-id="9ce37-120">_x_</span></span> <br/> |<span data-ttu-id="9ce37-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9ce37-121">Required</span></span>  <br/> |<span data-ttu-id="9ce37-122">**String**</span><span class="sxs-lookup"><span data-stu-id="9ce37-122">**String**</span></span> <br/> |<span data-ttu-id="9ce37-123">Una coordenada x.</span><span class="sxs-lookup"><span data-stu-id="9ce37-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="9ce37-124">_y_</span><span class="sxs-lookup"><span data-stu-id="9ce37-124">_y_</span></span> <br/> |<span data-ttu-id="9ce37-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9ce37-125">Required</span></span>  <br/> |<span data-ttu-id="9ce37-126">**String**</span><span class="sxs-lookup"><span data-stu-id="9ce37-126">**String**</span></span> <br/> |<span data-ttu-id="9ce37-127">Una coordenada y.</span><span class="sxs-lookup"><span data-stu-id="9ce37-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="9ce37-128">_opcional_</span><span class="sxs-lookup"><span data-stu-id="9ce37-128">_option_</span></span> <br/> |<span data-ttu-id="9ce37-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9ce37-129">Required</span></span>  <br/> |<span data-ttu-id="9ce37-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9ce37-130">**Boolean**</span></span> <br/> |<span data-ttu-id="9ce37-p101">Especifica la forma en que deben tratarse los puntos que caen en las diagonales. Especifique el valor 0 para usar los sectores izquierdo y derecho para los puntos que forman parte de una diagonal. Especifique el valor 1 para usar los sectores superior e inferior para los puntos que forman parte de una diagonal.</span><span class="sxs-lookup"><span data-stu-id="9ce37-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ce37-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ce37-134">Remarks</span></span>

<span data-ttu-id="9ce37-135">Considere un rectángulo con un *ancho* y un *alto* , y un punto (*x, y*) desde el punto central del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="9ce37-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="9ce37-136">Al trazar las diagonales que unen las esquinas del rectángulo, éste queda dividido en cuatro sectores y se define su centro.</span><span class="sxs-lookup"><span data-stu-id="9ce37-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="9ce37-137">Los sectores 0 al 4 representan, respectivamente, el centro del rectángulo y los sectores derecho, superior, izquierdo e inferior.</span><span class="sxs-lookup"><span data-stu-id="9ce37-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Los sectores del 0 al 4 representan respectivamente los puntos central, derecho, superior, izquierdo e inferior.](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="9ce37-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ce37-139">Example</span></span>

<span data-ttu-id="9ce37-140">RECTSECT(1 pda; 2 pda; 1 pda; -7 pda; 0)</span><span class="sxs-lookup"><span data-stu-id="9ce37-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="9ce37-141">Devuelve 4.</span><span class="sxs-lookup"><span data-stu-id="9ce37-141">Returns 4.</span></span> 
  

