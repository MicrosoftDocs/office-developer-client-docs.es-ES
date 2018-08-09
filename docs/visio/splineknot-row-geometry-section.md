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
description: Contiene x - e y-coordenadas de punto de control de una spline y un nodo de una spline.
ms.openlocfilehash: 297889208e064870dd37ed45a17fef7cb4b333b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823311"
---
# <a name="splineknot-row-geometry-section"></a>Fila SplineKnot (sección Geometría)

Contiene *x* - e *y* -coordenadas de punto de control de una spline y un nodo de una spline. 
  
Las filas SplineKnot contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La *x* -coordenadas de un punto de control.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La *y* -coordenadas de un punto de control.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Uno de los nodos de la spline (cualquiera menos el último o los dos primeros).  <br/> |
   
## <a name="remarks"></a>Comentarios

Visio muestra la definición de una spline en la sección de geometría que contiene una fila SplineStart seguida por una o varias filas SplineKnot. Antes de la fila SplineStart debe aparecer otro tipo de fila, como MoveTo, para indicar el primer punto de control de la spline. La fila anterior puede ser LineTo, ArcTo, NURBSTo, PolylineTo o EllipticalArcTo si la spline va detrás de un segmento de uno de esos tipos.
  

