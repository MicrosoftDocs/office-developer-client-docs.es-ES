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
description: Representa una coordenada x de una forma en coordenadas locales. En la tabla siguiente se describe la celda X según la fila en la que se encuentre.
ms.openlocfilehash: 6554000a86a6bf27d343a5647161bbe416725e64
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423947"
---
# <a name="x-cell-geometry-section"></a>Celda X (Sección de geometría)

Representa una coordenada *x* de una forma en coordenadas locales. En la tabla siguiente se describe la celda X según la fila en la que se encuentre. 
  
|**Row**|**Descripción**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Si la fila MoveTo es la primera fila de la sección, la celda X representa la coordenada *x* del primer vértice de una ruta de acceso. Si la fila MoveTo aparece entre dos filas, la celda X representa la coordenada *x* del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Coordenada *x* del vértice del extremo de un segmento de línea recta.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Coordenada *x* del vértice del extremo de un arco.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordenada *x* del vértice del extremo de un arco elíptico.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Coordenada *x* del vértice del extremo de una polilínea.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Coordenada *x* del último punto de control de una spline B racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Coordenada *x* del segundo punto de control de una spline.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Coordenada *x* de un punto de control.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordenada *x* de un punto de la línea infinita.  <br/> |
|[Origina](ellipse-row-geometry-section.md) <br/> | Coordenada *x* del centro de la elipse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . X *j* donde *i* y *j* = <1>, 2, 3...  <br/> |
|| Geometría *i* . X1 (filas InfiniteLine y Ellipse) donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda X por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex** +  *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (filas InfiniteLine y Ellipse)  <br/> |
| Índice de celda:  <br/> |**visX** (filas MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart y SplineKnot)  <br/> |
||**visInfiniteLineX1** (fila InfiniteLine)  <br/> |
||**visEllipseCenterX** (fila Ellipse)  <br/> |
   

