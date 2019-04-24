---
title: Fila EllipticalArcTo (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Contiene las coordenadas x e y del extremo de un arco elíptico, las coordenadas x e y de los puntos de control del arco, el ángulo desde el eje x hasta el eje principal de la elipse y la relación entre los ejes mayor y menor de la elipse.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345678"
---
# <a name="ellipticalarcto-row-geometry-section"></a>Fila EllipticalArcTo (Sección de Geometría)

Contiene las coordenadas *x* e y del extremo de un arco elíptico, las coordenadas *x* e ** y de los puntos de control del arco, el ángulo desde el eje *x* hasta el eje principal de la elipse y la relación entre el mayor y el Mino de la elipse. ** ejes r. 
  
Las filas EllipticalArcTo contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordenada *x* del vértice del extremo de un arco.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordenada *y* del vértice del extremo de un arco.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordenada *x* del punto de control del arco; un punto en el arco. El punto de control se encuentra mejor cerca de la mitad de la distancia entre los vértices inicial y final del arco. De lo contrario, el arco puede aumentar hasta un tamaño extremo a fin de pasar por el punto de control, con resultados imprevisibles.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordenada *y* del punto de control de un arco.  <br/> |
|[CA](c-cell-geometry-section.md) <br/> |Ángulo del eje mayor de un arco con respecto al eje *x* de su elemento primario.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Relación entre el eje mayor y el eje menor de un arco. A pesar del significado normal de estas palabras, el eje "mayor" no tiene por qué ser más grande que el eje "menor", por lo que esta relación no tiene que ser mayor que 1. Si establece en esta celda un valor menor o igual que 0, o mayor que 1000, pueden producirse resultados inesperados.  <br/> |
   

