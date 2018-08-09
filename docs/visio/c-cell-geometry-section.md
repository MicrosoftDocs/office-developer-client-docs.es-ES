---
title: Celda C (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Representa distinta información según las filas. En la tabla siguiente se describe la celda C según la fila en la que se encuentre.
ms.openlocfilehash: 1b9a813be825f2deeb5c90d596ffd9f3705bcef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821700"
---
# <a name="c-cell-geometry-section"></a>Celda C (sección Geometría)

Representa distinta información según las filas. En la tabla siguiente se describe la celda C según la fila en la que se encuentre.
  
|**Row**|**Descripción**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Ángulo del eje mayor de un arco con respecto a la *x* -eje de su forma principal.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Primer nodo de la spline B racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Último nodo de una spline.  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | Una *x* -coordenadas de un punto de una elipse; emparejada con la *y* -coordenada representada por la celda [d.](d-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda C por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . C *j* donde *i* y *j* = < 1 >, 2, 3...  <br/> |
|| Geometría *i* . C1 (fila Ellipse)  <br/> |
   
Para obtener una referencia a la celda C por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex** +  *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (fila Ellipse)  <br/> |
| Índice de celda:  <br/> |**visEccentricityAngle** (fila EllipticalArcTo)  <br/> |
||**visNURBSKnotPrev** (fila NURBSTo)  <br/> |
||**visSplineKnot3** (fila SplineStart)  <br/> |
||**visEllipseMinorX** (fila Ellipse)  <br/> |
   

