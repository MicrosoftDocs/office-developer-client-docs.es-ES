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
ms.openlocfilehash: a76093f028986907b58175bc6b8c81a7056cfe07
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542502"
---
# <a name="d-cell-geometry-section"></a>Celda D (sección de geometría)

Representa distinta información según las filas. En la tabla siguiente se describe la celda D según la fila en la que se encuentre.
  
|Row|Descripción|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Relación entre el eje mayor y el eje menor de un arco. A pesar del significado normal de estas palabras, el eje "mayor" no tiene por qué ser más grande que el eje "menor", por lo que esta relación no tiene que ser mayor que 1. Si establece en esta celda un valor menor o igual que 0, o mayor que 1000, pueden producirse resultados inesperados.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Primer grosor de la spline B racional no uniforme (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Grado de la spline (un número entero entre 1 y 25).  <br/> |
|[Origina](ellipse-row-geometry-section.md) <br/> | Coordenada *y* de un punto de una elipse; emparejado con la coordenada *x* representada por la celda [C](c-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Observaciones

Para obtener una referencia a la celda D por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . D *j* donde *i* y *j* = <1>, 2, 3...  <br/> |
|| Geometría *i* . D1 (fila Ellipse) donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda D por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowVertex** +  *j* donde *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (fila Ellipse)  <br/> |
| Índice de celda:  <br/> |**visAspectRatio** (fila EllipticalArcTo)  <br/> |
||**visNURBSWeightPrev** (fila NURBSTo)  <br/> |
||**visSplineDegree** (fila SplineStart)  <br/> |
||**visEllipseMinorY** (fila Ellipse)  <br/> |
   

