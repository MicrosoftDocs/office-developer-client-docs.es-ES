---
title: Sección de borrador
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
localization_priority: Normal
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: Un área de trabajo para escribir y probar fórmulas a las que hacen referencia otras celdas.
ms.openlocfilehash: a7d2c6762e96fc19986521c2ba164666b925c928
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411606"
---
# <a name="scratch-section"></a><span data-ttu-id="e22ad-103">Sección de borrador</span><span class="sxs-lookup"><span data-stu-id="e22ad-103">Scratch Section</span></span>

<span data-ttu-id="e22ad-104">Un área de trabajo para escribir y probar fórmulas a las que hacen referencia otras celdas.</span><span class="sxs-lookup"><span data-stu-id="e22ad-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e22ad-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e22ad-105">Remarks</span></span>

<span data-ttu-id="e22ad-p101">Puede agregar esta sección con el cuadro de diálogo **Insertar sección**. Haga clic con el botón secundario en la ventana ShapeSheet y, a continuación, haga clic en **Insertar sección**.</span><span class="sxs-lookup"><span data-stu-id="e22ad-p101">You can add this section by using the **Insert Section** dialog box. Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="e22ad-108">La **sección Scratch** se usa normalmente para aislar cálculos complejos repetidos.</span><span class="sxs-lookup"><span data-stu-id="e22ad-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="e22ad-109">Si la solución tiene un propósito bien definido, es más conveniente  usar una celda en la sección Celdas definidas por el usuario para mayor claridad, ya que las celdas de usuario se pueden nombrar.</span><span class="sxs-lookup"><span data-stu-id="e22ad-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="e22ad-110">Las celdas de **la sección Scratch** usan unidades de dos maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="e22ad-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="e22ad-111">Las celdas X e Y usan unidades de dibujo; Las celdas A a D no usan unidades.</span><span class="sxs-lookup"><span data-stu-id="e22ad-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="e22ad-112">(En la jerga de los programadores C, las celdas X e Y se "escriben" y las celdas A a D son "void"). Las celdas **Scratch X** y **Scratch Y** suelen usarse para derivar coordenadas *x* e *y,* como **PinX** y **PinY,** o las celdas X e Y que se encuentran en una celda de sección **Geometría.**</span><span class="sxs-lookup"><span data-stu-id="e22ad-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="e22ad-113">Las celdas de scratch A a D pueden mostrar las unidades que especifique.</span><span class="sxs-lookup"><span data-stu-id="e22ad-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="e22ad-114">Una diferencia mayor es la manera en que dichas celdas almacenan los valores de puntos.</span><span class="sxs-lookup"><span data-stu-id="e22ad-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="e22ad-115">Un punto de Visio es un único paquete de datos para una coordenada ( *x,y*).</span><span class="sxs-lookup"><span data-stu-id="e22ad-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="e22ad-116">Cuando una fórmula devuelve un punto, su valor se puede interpretar de tres maneras, dependiendo de la celda ShapeSheet donde esté la fórmula.</span><span class="sxs-lookup"><span data-stu-id="e22ad-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="e22ad-117">Las celdas que se relacionan con  *x*  -coordinates (por ejemplo, **PinX** o celdas de la columna X de una sección **Geometry)** extraen solo la  *parte x*  -coordinate de un valor de punto.</span><span class="sxs-lookup"><span data-stu-id="e22ad-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="e22ad-118">Las celdas relacionadas  *con y*  -coordinates extraen solo la  *parte y*  -coordinate de un valor de punto.</span><span class="sxs-lookup"><span data-stu-id="e22ad-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="e22ad-119">Por ejemplo, Visio extrae la fórmula `PNT(3,4)` de estas tres maneras.</span><span class="sxs-lookup"><span data-stu-id="e22ad-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="e22ad-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="e22ad-120">**Cell**</span></span>|<span data-ttu-id="e22ad-121">**Si escribe**</span><span class="sxs-lookup"><span data-stu-id="e22ad-121">**If you enter**</span></span>|<span data-ttu-id="e22ad-122">**Visio la trata como**</span><span class="sxs-lookup"><span data-stu-id="e22ad-122">**Visio treats it as**</span></span>|<span data-ttu-id="e22ad-123">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="e22ad-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e22ad-124">X</span><span class="sxs-lookup"><span data-stu-id="e22ad-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="e22ad-125">3,0000 pda.</span><span class="sxs-lookup"><span data-stu-id="e22ad-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="e22ad-126">v</span><span class="sxs-lookup"><span data-stu-id="e22ad-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="e22ad-127">4,0000 pda.</span><span class="sxs-lookup"><span data-stu-id="e22ad-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="e22ad-128">A-D</span><span class="sxs-lookup"><span data-stu-id="e22ad-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="e22ad-129">PNT(3.0000 in., 4.0000 in.)</span><span class="sxs-lookup"><span data-stu-id="e22ad-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

