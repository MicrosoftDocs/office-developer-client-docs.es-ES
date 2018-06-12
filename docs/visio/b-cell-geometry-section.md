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
ms.openlocfilehash: 7d6f51d037be4852c6a101ad6e576a3a13488cb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821552"
---
# <a name="b-cell-geometry-section"></a>Celda B (Sección de geometría)

Representa distinta información según las filas. En la tabla siguiente se describe la celda B según la fila en la que se encuentre.
  
|**Row**|**Descripción**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | La *y* -coordenadas del punto de control de un arco.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Último grosor de la spline B racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Primer nodo de una spline.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Un *y* -coordenadas de un punto de una línea infinita; emparejada con *x* -coordenada representada por la celda [A](a-cell-geometry-section.md) .  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | Un *y* -coordenadas de un punto de una elipse; emparejada con *x* -coordenada representada por la celda [A](a-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda B por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . B *j* donde *i* y *j* = < 1 >, 2, 3...  <br/> |
|| Geometría *i* . B1 (filas InfiniteLine y Ellipse)  <br/> |
   
Para obtener una referencia a la celda B por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex** +  *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Filas InfiniteLine y Ellipse)  <br/> |
| Índice de celda:  <br/> |**visControlX** (Fila EllipticalArcTo)  <br/> |
||**visControlY** (Fila EllipticalArcTo)  <br/> |
||**visNURBSWeight** (Fila NURBSTo)  <br/> |
||**visSplineKnot2** (Fila SplineStart)  <br/> |
||**visInfiniteLineY2** (Fila InfiniteLine)  <br/> |
||**visEllipseMajorY** (Fila ellipse)  <br/> |
   

