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
description: Representa una coordenada y de una forma en coordenadas locales. En la tabla siguiente se describe la celda Y según la fila en la que se encuentre.
ms.openlocfilehash: 9e823b8d21682b419a70ce498016abf575f36f6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342815"
---
# <a name="y-cell-geometry-section"></a>Celda Y (Sección de geometría)

Representa una coordenada *y* de una forma en coordenadas locales. En la tabla siguiente se describe la celda Y según la fila en la que se encuentre. 
  
|**Fila**|**Descripción**|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Si la fila MoveTo es la primera fila de la sección, la celda Y representa la coordenada *Y* del primer vértice de una ruta de acceso. Si la fila MoveTo aparece entre dos filas, la celda Y representa la coordenada *Y* del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Coordenada *y* del vértice del extremo de un segmento de línea recta.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Coordenada *y* del vértice del extremo de un arco.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordenada *y* del vértice del extremo de un arco elíptico.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Coordenada *y* del vértice del extremo de una polilínea.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Coordenada *y* del último punto de control de una spline B racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Coordenada *y* del segundo punto de control de una spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Coordenada *y* de un punto de control.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordenada *y* de un punto de la línea infinita.  <br/> |
|[Origina](ellipse-row-geometry-section.md) <br/> | Coordenada *y* del centro de la elipse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . Y *j* donde *i* y *j* = <1>, 2, 3...  <br/> |
|| Geometría *i* . Y1 (filas InfiniteLine y Ellipse) donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex** +  *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (filas InfiniteLine y Ellipse)  <br/> |
| Índice de celda:  <br/> |**visY** (filas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart y SplineKnot)  <br/> |
||**visInfiniteLineY1** (fila InfiniteLine)  <br/> |
||**visEllipseCenterY** (fila Ellipse)  <br/> |
   

