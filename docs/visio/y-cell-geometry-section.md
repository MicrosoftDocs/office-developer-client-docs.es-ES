---
title: Celda Y (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Representa una coordenada y en una forma en coordenadas locales. En la tabla siguiente se describe la celda Y según la fila en la que se encuentre.
ms.openlocfilehash: 7dea96b544c84f09abe1d72304da0bacaa09432f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540493"
---
# <a name="y-cell-geometry-section"></a>Celda Y (Sección de geometría)

Representa una  *coordenada y*  en una forma en coordenadas locales. En la tabla siguiente se describe la celda Y según la fila en la que se encuentre. 
  
|Fila|Descripción|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Si la fila MoveTo es la primera fila de la sección, la celda Y representa la coordenada  *y*  del primer vértice de una ruta de acceso. Si la fila MoveTo aparece entre dos filas, la celda Y representa la coordenada  *y*  del primer vértice después del salto en la ruta de acceso.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | *Coordenada y* del vértice final de un segmento de línea recta.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | *Coordenada y* del vértice final de un arco.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | *Coordenada y* del vértice final de un arco elíptico.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | *Coordenada y* del vértice final de una polilínea.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Coordenada  *y*  del último punto de control de una spline B racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Coordenada  *y*  del segundo punto de control de una spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | *Coordenada y* de un punto de control.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | *Coordenada y* de un punto en la línea infinita.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | Coordenada  *y*  del centro de la elipse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría  *i*  . Y  *j*            donde  *i*  y  *j*  = <1>, 2, 3...  <br/> |
|| Geometría  *i*  . Y1 (filas InfiniteLine y Ellipse) donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex**  +   *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (filas InfiniteLine y Ellipse)  <br/> |
| Índice de celda:  <br/> |**visY** (filas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart y SplineKnot)  <br/> |
||**visInfiniteLineY1** (fila InfiniteLine)  <br/> |
||**visEllipseCenterY** (fila Ellipse)  <br/> |
   

