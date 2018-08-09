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
ms.openlocfilehash: 16f0bac8f139c0b03d7826ac377a964d15296dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823107"
---
# <a name="scratch-section"></a><span data-ttu-id="bdbf4-103">Sección Borrador</span><span class="sxs-lookup"><span data-stu-id="bdbf4-103">Scratch Section</span></span>

<span data-ttu-id="bdbf4-104">Un área de trabajo para escribir y probar fórmulas a las que hacen referencia otras celdas.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bdbf4-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdbf4-105">Remarks</span></span>

<span data-ttu-id="bdbf4-p101">Puede agregar esta sección con el cuadro de diálogo **Insertar sección**. Haga clic con el botón secundario en la ventana ShapeSheet y, a continuación, haga clic en **Insertar sección**.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-p101">You can add this section by using the **Insert Section** dialog box. Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="bdbf4-108">La sección **de borrador** se usa normalmente para aislar cálculos complejos que se repiten.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="bdbf4-109">Si su solución tiene un propósito bien definido, es mejor utilizar una celda de la sección **User-Defined Cells** para mayor claridad, debido a que las celdas de usuario pueden tener nombre.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="bdbf4-110">Las celdas en la sección **de borrador** utilizan unidades de dos maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="bdbf4-111">Las celdas X e Y utilizan unidades de dibujo; Un a celdas D no utiliza unidades.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="bdbf4-112">(En Scratch, las celdas X e Y se "ha escrito", y las celdas de la A la D son "void".) Las celdas Scratch **X** y **Scratch Y** a menudo se usan para derivar coordenadas *x* e *y* , como **PinX** y **PinY**o las celdas X e Y que se encuentra en una celda de la sección de **geometría** .</span><span class="sxs-lookup"><span data-stu-id="bdbf4-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="bdbf4-113">Scratch celdas a la D puede mostrar cualquier unidad que especifique.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="bdbf4-114">Una diferencia mayor es la manera en que dichas celdas almacenan los valores de punto.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="bdbf4-115">Un punto en Visio es un paquete de datos para una coordenada ( *x, y*).</span><span class="sxs-lookup"><span data-stu-id="bdbf4-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="bdbf4-116">Cuando una fórmula devuelve un valor de punto, ese valor se interpreta en uno de tres maneras, dependiendo de la celda ShapeSheet en que la fórmula es.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="bdbf4-117">Las celdas que se relacionan con *x* -coordenadas (por ejemplo, **PinX**o las celdas de la columna X de una sección de **geometría** ) extracción sólo la *x* -coordinar parte de un valor en puntos.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="bdbf4-118">Las celdas que se relacionan con *y* -coordenadas extracción sólo la *y* -coordinar parte de un valor en puntos.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="bdbf4-119">Por ejemplo, Visio extrae la fórmula `PNT(3,4)` de estas tres maneras.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="bdbf4-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="bdbf4-120">**Cell**</span></span>|<span data-ttu-id="bdbf4-121">**Si escribe**</span><span class="sxs-lookup"><span data-stu-id="bdbf4-121">**If you enter**</span></span>|<span data-ttu-id="bdbf4-122">**Visio la trata como**</span><span class="sxs-lookup"><span data-stu-id="bdbf4-122">**Visio treats it as**</span></span>|<span data-ttu-id="bdbf4-123">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="bdbf4-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bdbf4-124">X</span><span class="sxs-lookup"><span data-stu-id="bdbf4-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="bdbf4-125">3,0000 pda.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="bdbf4-126">Y</span><span class="sxs-lookup"><span data-stu-id="bdbf4-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="bdbf4-127">4,0000 pda.</span><span class="sxs-lookup"><span data-stu-id="bdbf4-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="bdbf4-128">A-D</span><span class="sxs-lookup"><span data-stu-id="bdbf4-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="bdbf4-129">PNT (3,0000 pda., 4,0000 pda.)</span><span class="sxs-lookup"><span data-stu-id="bdbf4-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

