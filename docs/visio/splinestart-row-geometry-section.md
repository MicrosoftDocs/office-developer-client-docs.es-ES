---
title: Fila SplineStart (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Contiene x - e y-coordenadas para el segundo punto de control de una spline, sus nodos segundo, primero, el último nodo y el grado de la spline.
ms.openlocfilehash: 0944da12e6090fde41dc5927b5705e103d29f76d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823313"
---
# <a name="splinestart-row-geometry-section"></a>Fila SplineStart (sección Geometría)

Contiene *x* - e *y* -coordenadas para el segundo punto de control de una spline, sus nodos segundo, primero, el último nodo y el grado de la spline. 
  
Las filas SplineStart contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La *x* -coordenadas del segundo punto de control de una spline.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La *y* -coordenadas del segundo punto de control de una spline.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Segundo nodo de la spline.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Primer nodo de una spline.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Último nodo de una spline.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Grado de la spline (un número entero entre 1 y 25).  <br/> |
   
## <a name="remarks"></a>Comentarios

Visio muestra la definición de una spline en la sección de geometría que contiene una fila SplineStart seguida por una o varias filas SplineKnot. Antes de la fila SplineStart debe aparecer otro tipo de fila, como MoveTo, para indicar el primer punto de control de la spline. La fila anterior puede ser LineTo, ArcTo, NURBSTo, PolylineTo o EllipticalArcTo si la spline va detrás de un segmento de uno de esos tipos.
  

