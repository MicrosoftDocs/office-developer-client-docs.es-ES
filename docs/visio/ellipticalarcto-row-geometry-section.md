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
description: Contiene x - e y-coordenadas del extremo de un arco elíptico, x e y-las coordenadas de los puntos de control del arco, ángulo desde la x-eje al eje de la elipse y la relación entre los ejes mayor y menor de la elipse.
ms.openlocfilehash: 9a356429f14a20b72a8bd55689855e2954d4a807
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822056"
---
# <a name="ellipticalarcto-row-geometry-section"></a>Fila EllipticalArcTo (Sección de Geometría)

Contiene *x* - e *y* - coordenadas del extremo de un arco elíptico, *x* - e *y* -las coordenadas de los puntos de control del arco, ángulo desde *x* -eje al eje de la elipse y la relación entre los principales de la elipse y Minor ejes de r. 
  
Las filas EllipticalArcTo contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La *x* -coordenadas del vértice del extremo de un arco.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La *y* -coordenadas del vértice del extremo de un arco.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |La *x* -coordenadas del punto de control del arco; un punto en el arco. El punto de control es mejor encuentra acerca de la mitad de la distancia entre el principio y el vértice final del arco. De lo contrario, el arco puede crecer demasiado para pasar por el punto de control, con resultados impredecibles.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |La *y* -coordenadas del punto de control de un arco.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Ángulo del eje mayor de un arco con respecto a la *x* -eje de su forma principal.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Relación entre el eje mayor y el eje menor de un arco. A pesar del significado normal de estas palabras, el eje "mayor" no tiene por qué ser más grande que el eje "menor", por lo que esta relación no tiene que ser mayor que 1. Si establece en esta celda un valor menor o igual que 0, o mayor que 1000, pueden producirse resultados inesperados.  <br/> |
   

