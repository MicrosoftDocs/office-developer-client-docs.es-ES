---
title: Celda X (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Representa una coordenada x en una forma en coordenadas locales. En la tabla siguiente se describe la celda X según la fila en la que se encuentre.
ms.openlocfilehash: 2b3303533db446780ef797844ac5e1438cec242f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538217"
---
# <a name="x-cell-geometry-section"></a>Celda X (Sección de geometría)

Representa una coordenada  *x*  en una forma en coordenadas locales. En la tabla siguiente se describe la celda X según la fila en la que se encuentre. 
  
|Fila|Descripción|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Si la fila MoveTo es la primera fila de la sección, la celda X representa la coordenada  *x*  del primer vértice de una ruta de acceso. Si la fila MoveTo aparece entre dos filas, la celda X representa la coordenada  *x*  del primer vértice después del salto en la ruta de acceso.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | La coordenada  *x*  del vértice final de un segmento de línea recta.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Coordenada  *x*  del vértice final de un arco.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | La coordenada  *x*  del vértice final de un arco elíptico.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | La coordenada  *x*  del vértice final de una polilínea.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | La coordenada  *x*  del último punto de control de una spline B racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Coordenada  *x*  del segundo punto de control de una spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | La coordenada  *x*  de un punto de control.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Una coordenada  *x*  de un punto en la línea infinita.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | La coordenada  *x*  del centro de la elipse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría  *i*  . X  *j*            donde  *i*  y  *j*  = <1>, 2, 3...  <br/> |
|| Geometría  *i*  . X1 (filas InfiniteLine y Ellipse) donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda X por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex**  +   *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (filas InfiniteLine y Ellipse)  <br/> |
| Índice de celda:  <br/> |**visX** (filas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart y SplineKnot)  <br/> |
||**visInfiniteLineX1** (fila InfiniteLine)  <br/> |
||**visEllipseCenterX** (fila Ellipse)  <br/> |
   

