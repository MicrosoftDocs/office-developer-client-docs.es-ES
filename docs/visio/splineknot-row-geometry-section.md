---
title: Fila SplineKnot (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Contiene las coordenadas x - e y para el punto de control de una spline y el nudo de una spline.
ms.openlocfilehash: 432b714772d96e0ab0861bbfb62075258404e607
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407420"
---
# <a name="splineknot-row-geometry-section"></a>Fila SplineKnot (Sección de Geometría)

Contiene  *las coordenadas x*  - e  *y*  para el punto de control de una spline y el nudo de una spline. 
  
Las filas SplineKnot contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La coordenada  *x*  de un punto de control.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Coordenada y* de un punto de control.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Uno de los nodos de la spline (cualquiera menos el último o los dos primeros).  <br/> |
   
## <a name="remarks"></a>Comentarios

Visio muestra la definición de una spline en la sección de geometría que contiene una fila SplineStart seguida por una o varias filas SplineKnot. Antes de la fila SplineStart debe aparecer otro tipo de fila, como MoveTo, para indicar el primer punto de control de la spline. La fila anterior puede ser LineTo, ArcTo, NURBSTo, PolylineTo o EllipticalArcTo si la spline va detrás de un segmento de uno de esos tipos.
  

