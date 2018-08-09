---
title: Celda D (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Representa distinta información según las filas. En la tabla siguiente se describe la celda D según la fila en la que se encuentre.
ms.openlocfilehash: ed67197e46ee159ba2175b0e86623fe1704992d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821894"
---
# <a name="d-cell-geometry-section"></a>Celda D (sección Geometría)

Representa distinta información según las filas. En la tabla siguiente se describe la celda D según la fila en la que se encuentre.
  
|**Row**|**Descripción**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Relación entre el eje mayor y el eje menor de un arco. A pesar del significado normal de estas palabras, el eje "mayor" no tiene por qué ser más grande que el eje "menor", por lo que esta relación no tiene que ser mayor que 1. Si establece en esta celda un valor menor o igual que 0, o mayor que 1000, pueden producirse resultados inesperados.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Primer grosor de la spline B racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Grado de la spline (un número entero entre 1 y 25).  <br/> |
|[Elipse](ellipse-row-geometry-section.md) <br/> | Un *y* -coordenadas de un punto de una elipse; emparejada con la *x* -representada por la celda [C](c-cell-geometry-section.md) de coordenadas.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda D por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . D *j* donde *i* y *j* = < 1 >, 2, 3...  <br/> |
|| Geometría *i* . D1 (fila Ellipse) donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda D por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex** +  *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (fila Ellipse)  <br/> |
| Índice de celda:  <br/> |**visAspectRatio** (fila EllipticalArcTo)  <br/> |
||**visNURBSWeightPrev** (fila NURBSTo)  <br/> |
||**visSplineDegree** (fila SplineStart)  <br/> |
||**visEllipseMinorY** (fila Ellipse)  <br/> |
   

