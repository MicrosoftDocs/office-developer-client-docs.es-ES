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
ms.openlocfilehash: 1f35704cdb827c9c751f11593436c110755d7777
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822903"
---
# <a name="rectsect-function"></a><span data-ttu-id="24970-103">Función RECTSECT</span><span class="sxs-lookup"><span data-stu-id="24970-103">RECTSECT Function</span></span>

<span data-ttu-id="24970-104">Calcula el sector de un rectángulo asociado a *x* e *y* y devuelve un número entero entre 0 y 4, que indica el sector.</span><span class="sxs-lookup"><span data-stu-id="24970-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="24970-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24970-105">Syntax</span></span>

<span data-ttu-id="24970-106">RECTSECT (** *ancho* **, ** *alto* **, ** *x* **, ** *y* **, ** *opción* **)</span><span class="sxs-lookup"><span data-stu-id="24970-106">RECTSECT(** *width* **, ** *height* **, ** *x* **, ** *y* **, ** *option* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="24970-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24970-107">Parameters</span></span>

|<span data-ttu-id="24970-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="24970-108">**Name**</span></span>|<span data-ttu-id="24970-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="24970-109">**Required/Optional**</span></span>|<span data-ttu-id="24970-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="24970-110">**Data Type**</span></span>|<span data-ttu-id="24970-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="24970-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="24970-112">_width_</span><span class="sxs-lookup"><span data-stu-id="24970-112">_width_</span></span> <br/> |<span data-ttu-id="24970-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="24970-113">Required</span></span>  <br/> |<span data-ttu-id="24970-114">**String**</span><span class="sxs-lookup"><span data-stu-id="24970-114">**String**</span></span> <br/> |<span data-ttu-id="24970-115">El ancho del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="24970-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="24970-116">_height_</span><span class="sxs-lookup"><span data-stu-id="24970-116">_height_</span></span> <br/> |<span data-ttu-id="24970-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="24970-117">Required</span></span>  <br/> |<span data-ttu-id="24970-118">**String**</span><span class="sxs-lookup"><span data-stu-id="24970-118">**String**</span></span> <br/> |<span data-ttu-id="24970-119">El alto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="24970-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="24970-120">_x_</span><span class="sxs-lookup"><span data-stu-id="24970-120">_x_</span></span> <br/> |<span data-ttu-id="24970-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="24970-121">Required</span></span>  <br/> |<span data-ttu-id="24970-122">**String**</span><span class="sxs-lookup"><span data-stu-id="24970-122">**String**</span></span> <br/> |<span data-ttu-id="24970-123">Una coordenada x.</span><span class="sxs-lookup"><span data-stu-id="24970-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="24970-124">_y_</span><span class="sxs-lookup"><span data-stu-id="24970-124">_y_</span></span> <br/> |<span data-ttu-id="24970-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="24970-125">Required</span></span>  <br/> |<span data-ttu-id="24970-126">**String**</span><span class="sxs-lookup"><span data-stu-id="24970-126">**String**</span></span> <br/> |<span data-ttu-id="24970-127">Una coordenada y.</span><span class="sxs-lookup"><span data-stu-id="24970-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="24970-128">_opción_</span><span class="sxs-lookup"><span data-stu-id="24970-128">_option_</span></span> <br/> |<span data-ttu-id="24970-129">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="24970-129">Required</span></span>  <br/> |<span data-ttu-id="24970-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="24970-130">**Boolean**</span></span> <br/> |<span data-ttu-id="24970-p101">Especifica la forma en que deben tratarse los puntos que caen en las diagonales. Especifique el valor 0 para usar los sectores izquierdo y derecho para los puntos que forman parte de una diagonal. Especifique el valor 1 para usar los sectores superior e inferior para los puntos que forman parte de una diagonal.</span><span class="sxs-lookup"><span data-stu-id="24970-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24970-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24970-134">Remarks</span></span>

<span data-ttu-id="24970-135">Considere la posibilidad de un rectángulo que tiene un *ancho* y un *alto* y un punto (*x, y*) desde el punto central del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="24970-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="24970-136">Dibuja líneas diagonales a través de las esquinas del rectángulo que se va a dividir en cuatro sectores y un punto central.</span><span class="sxs-lookup"><span data-stu-id="24970-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="24970-137">Los sectores 0 al 4 representan el punto central, derecha, arriba, izquierda y abajo respectivamente.</span><span class="sxs-lookup"><span data-stu-id="24970-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="24970-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="24970-138">Example</span></span>

<span data-ttu-id="24970-139">RECTSECT(1 pda; 2 pda; 1 pda; -7 pda; 0)</span><span class="sxs-lookup"><span data-stu-id="24970-139">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="24970-140">Devuelve 4.</span><span class="sxs-lookup"><span data-stu-id="24970-140">Returns 4.</span></span> 
  

