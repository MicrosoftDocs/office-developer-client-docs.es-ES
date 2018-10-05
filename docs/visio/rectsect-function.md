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
description: Calcula el sector de un rectángulo asociado a x e y y devuelve un número entero entre 0 y 4, que indica el sector.
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395087"
---
# <a name="rectsect-function"></a><span data-ttu-id="59e53-103">Función RECTSECT</span><span class="sxs-lookup"><span data-stu-id="59e53-103">RECTSECT Function</span></span>

<span data-ttu-id="59e53-104">Calcula el sector de un rectángulo asociado a *x* e *y* y devuelve un número entero entre 0 y 4, que indica el sector.</span><span class="sxs-lookup"><span data-stu-id="59e53-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="59e53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59e53-105">Syntax</span></span>

<span data-ttu-id="59e53-106">RECTSECT (\*\* *ancho* \*\*, \*\* *alto* \*\*, \*\* *x* \*\*, \*\* *y* \*\*, \*\* *opción* \*\*)</span><span class="sxs-lookup"><span data-stu-id="59e53-106">RECTSECT(\*\* *width* \*\*, \*\* *height* \*\*, \*\* *x* \*\*, \*\* *y* \*\*, \*\* *option* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="59e53-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59e53-107">Parameters</span></span>

|<span data-ttu-id="59e53-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="59e53-108">**Name**</span></span>|<span data-ttu-id="59e53-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="59e53-109">**Required/Optional**</span></span>|<span data-ttu-id="59e53-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="59e53-110">**Data Type**</span></span>|<span data-ttu-id="59e53-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59e53-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="59e53-112">_width_</span><span class="sxs-lookup"><span data-stu-id="59e53-112">_width_</span></span> <br/> |<span data-ttu-id="59e53-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59e53-113">Required</span></span>  <br/> |<span data-ttu-id="59e53-114">**String**</span><span class="sxs-lookup"><span data-stu-id="59e53-114">**String**</span></span> <br/> |<span data-ttu-id="59e53-115">El ancho del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="59e53-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="59e53-116">_height_</span><span class="sxs-lookup"><span data-stu-id="59e53-116">_height_</span></span> <br/> |<span data-ttu-id="59e53-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59e53-117">Required</span></span>  <br/> |<span data-ttu-id="59e53-118">**String**</span><span class="sxs-lookup"><span data-stu-id="59e53-118">**String**</span></span> <br/> |<span data-ttu-id="59e53-119">El alto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="59e53-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="59e53-120">_x_</span><span class="sxs-lookup"><span data-stu-id="59e53-120">_x_</span></span> <br/> |<span data-ttu-id="59e53-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59e53-121">Required</span></span>  <br/> |<span data-ttu-id="59e53-122">**String**</span><span class="sxs-lookup"><span data-stu-id="59e53-122">**String**</span></span> <br/> |<span data-ttu-id="59e53-123">Una coordenada x.</span><span class="sxs-lookup"><span data-stu-id="59e53-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="59e53-124">_y_</span><span class="sxs-lookup"><span data-stu-id="59e53-124">_y_</span></span> <br/> |<span data-ttu-id="59e53-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59e53-125">Required</span></span>  <br/> |<span data-ttu-id="59e53-126">**String**</span><span class="sxs-lookup"><span data-stu-id="59e53-126">**String**</span></span> <br/> |<span data-ttu-id="59e53-127">Una coordenada y.</span><span class="sxs-lookup"><span data-stu-id="59e53-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="59e53-128">_opción_</span><span class="sxs-lookup"><span data-stu-id="59e53-128">_option_</span></span> <br/> |<span data-ttu-id="59e53-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="59e53-129">Required</span></span>  <br/> |<span data-ttu-id="59e53-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="59e53-130">**Boolean**</span></span> <br/> |<span data-ttu-id="59e53-p101">Especifica la forma en que deben tratarse los puntos que caen en las diagonales. Especifique el valor 0 para usar los sectores izquierdo y derecho para los puntos que forman parte de una diagonal. Especifique el valor 1 para usar los sectores superior e inferior para los puntos que forman parte de una diagonal.</span><span class="sxs-lookup"><span data-stu-id="59e53-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59e53-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59e53-134">Remarks</span></span>

<span data-ttu-id="59e53-135">Considere la posibilidad de un rectángulo que tiene un *ancho* y un *alto* y un punto (*x, y*) desde el punto central del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="59e53-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="59e53-136">Dibuja líneas diagonales a través de las esquinas del rectángulo que se va a dividir en cuatro sectores y un punto central.</span><span class="sxs-lookup"><span data-stu-id="59e53-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="59e53-137">Los sectores 0 al 4 representan el punto central, derecha, arriba, izquierda y abajo respectivamente.</span><span class="sxs-lookup"><span data-stu-id="59e53-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Sectores 0 al 4 representan el punto central, derecha, arriba, izquierda y abajo, respectivamente](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="59e53-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59e53-139">Example</span></span>

<span data-ttu-id="59e53-140">RECTSECT(1 pda; 2 pda; 1 pda; -7 pda; 0)</span><span class="sxs-lookup"><span data-stu-id="59e53-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="59e53-141">Devuelve 4.</span><span class="sxs-lookup"><span data-stu-id="59e53-141">Returns 4.</span></span> 
  

