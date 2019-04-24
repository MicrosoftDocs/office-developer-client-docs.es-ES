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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344530"
---
# <a name="scratch-section"></a><span data-ttu-id="628c3-103">Sección de borrador</span><span class="sxs-lookup"><span data-stu-id="628c3-103">Scratch Section</span></span>

<span data-ttu-id="628c3-104">Un área de trabajo para escribir y probar fórmulas a las que hacen referencia otras celdas.</span><span class="sxs-lookup"><span data-stu-id="628c3-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="628c3-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="628c3-105">Remarks</span></span>

<span data-ttu-id="628c3-p101">Puede agregar esta sección con el cuadro de diálogo **Insertar sección**. Haga clic con el botón secundario en la ventana ShapeSheet y, a continuación, haga clic en **Insertar sección**.</span><span class="sxs-lookup"><span data-stu-id="628c3-p101">You can add this section by using the **Insert Section** dialog box. Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="628c3-108">La \*\*\*\* sección de borrador suele usarse para aislar cálculos complejos repetidos.</span><span class="sxs-lookup"><span data-stu-id="628c3-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="628c3-109">Si la solución tiene un propósito bien definido, es Wiser usar una celda de la sección de **celdas definidas por el usuario** para lograr una mayor claridad porque se pueden asignar nombres a las celdas de usuario.</span><span class="sxs-lookup"><span data-stu-id="628c3-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="628c3-110">Las celdas de la sección **Scratch** usan unidades de dos maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="628c3-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="628c3-111">Las celdas X e y usan unidades de dibujo; Las celdas de la a a la D no usan unidades.</span><span class="sxs-lookup"><span data-stu-id="628c3-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="628c3-112">(En la jerga de los programadores de C, las celdas X e y se "escriben" y las celdas de la a a la D son "Void".) Las **celdas Scratch x** y **Scratch** y se suelen usar para derivar coordenadas *x* e \*\* y, como **PinX** y **PinY**, o las celdas x e y que se encuentran en una celda de la sección **Geometry** .</span><span class="sxs-lookup"><span data-stu-id="628c3-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="628c3-113">Las celdas de grietas de la a a la D pueden mostrar las unidades que especifique.</span><span class="sxs-lookup"><span data-stu-id="628c3-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="628c3-114">Una diferencia mayor es la manera en que dichas celdas almacenan los valores de puntos.</span><span class="sxs-lookup"><span data-stu-id="628c3-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="628c3-115">Un punto en Visio es un paquete de datos único para una coordenada ( *x, y*).</span><span class="sxs-lookup"><span data-stu-id="628c3-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="628c3-116">Cuando una fórmula devuelve un punto, su valor se puede interpretar de tres maneras, dependiendo de la celda ShapeSheet donde esté la fórmula.</span><span class="sxs-lookup"><span data-stu-id="628c3-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="628c3-117">Las celdas relacionadas con las coordenadas *x* (por ejemplo, **PinX**o las celdas de la columna x de una sección **Geometry** ) extraen sólo la parte *x* -coordinada de un valor Point.</span><span class="sxs-lookup"><span data-stu-id="628c3-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="628c3-118">Las celdas relacionadas con las coordenadas *y* extraen sólo la parte de coordenada *y* de un valor de punto.</span><span class="sxs-lookup"><span data-stu-id="628c3-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="628c3-119">Por ejemplo, Visio extrae la `PNT(3,4)` fórmula de estas tres formas.</span><span class="sxs-lookup"><span data-stu-id="628c3-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="628c3-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="628c3-120">**Cell**</span></span>|<span data-ttu-id="628c3-121">**Si escribe**</span><span class="sxs-lookup"><span data-stu-id="628c3-121">**If you enter**</span></span>|<span data-ttu-id="628c3-122">**Visio la trata como**</span><span class="sxs-lookup"><span data-stu-id="628c3-122">**Visio treats it as**</span></span>|<span data-ttu-id="628c3-123">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="628c3-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="628c3-124">X</span><span class="sxs-lookup"><span data-stu-id="628c3-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="628c3-125">3,0000 pda.</span><span class="sxs-lookup"><span data-stu-id="628c3-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="628c3-126">v</span><span class="sxs-lookup"><span data-stu-id="628c3-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="628c3-127">4,0000 pda.</span><span class="sxs-lookup"><span data-stu-id="628c3-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="628c3-128">A-D</span><span class="sxs-lookup"><span data-stu-id="628c3-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="628c3-129">PNT (3.0000 in., 4,0000)</span><span class="sxs-lookup"><span data-stu-id="628c3-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

