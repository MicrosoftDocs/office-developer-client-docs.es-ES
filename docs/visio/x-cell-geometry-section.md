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
description: Representa una x-coordenadas en una forma en coordenadas locales. En esta tabla se describe la celda X según la fila en la que se encuentre.
ms.openlocfilehash: e5bc99d4f73d49741c4378009dfc2a883bb655ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823560"
---
# <a name="x-cell-geometry-section"></a>Celda X (Sección de geometría)

Representa una *x* -coordenadas en una forma en coordenadas locales. En esta tabla se describe la celda X según la fila en la que se encuentre. 
  
|**Row**|**Descripción**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Si la fila MoveTo es la primera fila en la sección, la celda X representa la *x* -coordenadas del primer vértice de una ruta de acceso. Si la fila MoveTo aparece entre dos filas, la celda X representa la *x* -coordenadas del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | La *x* -coordenadas del vértice del extremo de un segmento de línea recta.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | La *x* -coordenadas del vértice del extremo de un arco.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | La *x* -coordenadas del vértice del extremo de un arco elíptico.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | La *x* -coordenadas del vértice del extremo de una polilínea.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | La *x* -coordenadas del último punto de control de una B-spline racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | La *x* -coordenadas del segundo punto de control de una spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | La *x* -coordenadas de un punto de control.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Una *x* -coordenadas de un punto de la línea infinita.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | La *x* -coordenadas del centro de la elipse.  <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . X *j* donde *i* y *j* = < 1 >, 2, 3...  <br/> |
|| Geometría *i* . X1 (filas InfiniteLine y Ellipse) donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda X por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex** +  *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Filas InfiniteLine y Ellipse)  <br/> |
| Índice de celda:  <br/> |**visX** (Filas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart y SplineKnot)  <br/> |
||**visInfiniteLineX1** (Fila InfiniteLine)  <br/> |
||**visEllipseCenterX** (Fila ellipse)  <br/> |
   

