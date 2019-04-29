---
title: Celda B (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Representa distinta información según las filas. En la tabla siguiente se describe la celda B según la fila en la que se encuentre.
ms.openlocfilehash: ff032b5af2918ec9865360ede5c3d76e8e872e9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423310"
---
# <a name="b-cell-geometry-section"></a>Celda B (sección de geometría)

Representa distinta información según las filas. En la tabla siguiente se describe la celda B según la fila en la que se encuentre.
  
|**Row**|**Descripción**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Coordenada *y* del punto de control de un arco.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Último grosor de la spline B racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Primer nodo de una spline.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Coordenada *y* de un punto de una línea infinita; emparejado con la coordenada *x* representada por la celda [A](a-cell-geometry-section.md) .  <br/> |
|[Origina](ellipse-row-geometry-section.md) <br/> | Coordenada *y* de un punto de una elipse; emparejado con la coordenada *x* representada por la celda [A](a-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda B por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . B *j* donde *i* y *j* = <1>, 2, 3...  <br/> |
|| Geometría *i* . B1 (filas InfiniteLine y Ellipse)  <br/> |
   
Para obtener una referencia a la celda B por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex** +  *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (filas InfiniteLine y Ellipse)  <br/> |
| Índice de celda:  <br/> |**visControlX** (fila EllipticalArcTo)  <br/> |
||**visControlY** (fila EllipticalArcTo)  <br/> |
||**visNURBSWeight** (fila NURBSTo)  <br/> |
||**visSplineKnot2** (fila SplineStart)  <br/> |
||**visInfiniteLineY2** (fila InfiniteLine)  <br/> |
||**visEllipseMajorY** (fila Ellipse)  <br/> |
   

