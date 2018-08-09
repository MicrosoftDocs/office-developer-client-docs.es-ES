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
description: Representa una y-coordenadas en una forma en coordenadas locales. En esta tabla se describe la celda Y según la fila en la que se encuentre.
ms.openlocfilehash: 461fd0ec41d34132f469c811292550d2f7e094f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823595"
---
# <a name="y-cell-geometry-section"></a>Celda Y (sección Geometría)

Representa una *y* -coordenadas en una forma en coordenadas locales. En esta tabla se describe la celda Y según la fila en la que se encuentre. 
  
|**Row**|**Descripción**|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Si la fila MoveTo es la primera fila en la sección, la celda Y representa la *y* -coordenadas del primer vértice de una ruta de acceso. Si la fila MoveTo aparece entre dos filas, la celda Y representa la *y* -coordenadas del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | La *y* -coordenadas del vértice del extremo de un segmento de línea recta.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | La *y* -coordenadas del vértice del extremo de un arco.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | La *y* -coordenadas del vértice del extremo de un arco elíptico.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | La *y* -coordenadas del vértice del extremo de una polilínea.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | La *y* -coordenadas del último punto de control de una B-spline racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | La *y* -coordenadas del segundo punto de control de una spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | La *y* -coordenadas de un punto de control.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Una coordenada *y* de un punto de la línea infinita.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | La *y* -coordenadas del centro de la elipse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . Y *j* donde *i* y *j* = < 1 >, 2, 3...  <br/> |
|| Geometría *i* . Y1 (filas InfiniteLine y Ellipse) donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Y por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex** +  *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (filas InfiniteLine y Ellipse)  <br/> |
| Índice de celda:  <br/> |**visY** (filas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart y SplineKnot)  <br/> |
||**visInfiniteLineY1** (fila InfiniteLine)  <br/> |
||**visEllipseCenterY** (fila Ellipse)  <br/> |
   

