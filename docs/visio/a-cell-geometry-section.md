---
title: Celda A (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Representa distinta información según las filas. En la tabla siguiente se describe la celda A según la fila en la que se encuentre.
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541305"
---
# <a name="a-cell-geometry-section"></a>Celda A (Sección de geometría)

Representa distinta información según las filas. En la tabla siguiente se describe la celda A según la fila en la que se encuentre.
  
|Fila|Descripción|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Distancia desde el punto medio del arco hasta el punto medio de su cuerda.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | La coordenada  *x*  del punto de control del arco, un punto en el arco. El punto de control se encuentra mejor a medio camino entre los vértices inicial y final del arco. De lo contrario, el arco puede crecer hasta un tamaño extremo para pasar a través del punto de control, con resultados impredecibles.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Fórmula de polilínea.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Penúltimo nodo de la spline B racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Segundo nodo de la spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Uno de los nodos de la spline (cualquiera menos el último o los dos primeros).  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Una coordenada *x* de un punto en la línea infinita; emparejado con *y* -coordinate representado por la [celda B.](b-cell-geometry-section.md)  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | Una coordenada *x* de un punto en la elipse; emparejado con *y* -coordinate representado por la [celda B.](b-cell-geometry-section.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda A por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría  *i*  . A  *j*            donde  *i*  y  *j*  = <1>, 2, 3...  <br/> |
|| Geometría  *i*  . A1 (filas InfiniteLine y Ellipse) donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia a la celda A por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex**  +   *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (filas InfiniteLine y Ellipse)  <br/> |
| Índice de celda:  <br/> |**visBow** (fila ArcTo)  <br/> |
||**visControlX** (fila EllipticalArcTo)  <br/> |
||**visControlY** (fila EllipticalArcTo)  <br/> |
||**visPolylineData** (fila Polyline)  <br/> |
||**visNURBSKnot** (fila NURBSTo)  <br/> |
||**visSplineKnot** (filas SplineStart y SplineKnot)  <br/> |
||**visInfiniteLineX2** (fila InfiniteLine)  <br/> |
||**visEllipseMajorX** (fila Ellipse)  <br/> |
   

