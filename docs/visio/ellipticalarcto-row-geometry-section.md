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
description: Contiene las coordenadas x - e y del extremo de un arco elíptico, x - e y -coordenadas de los puntos de control en el arco, ángulo desde el eje x al eje principal de la elipse y relación entre los ejes principales y los ejes menores de la elipse.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421406"
---
# <a name="ellipticalarcto-row-geometry-section"></a>Fila EllipticalArcTo (Sección de Geometría)

Contiene las coordenadas  *x*  -  *e y*  del extremo de un arco elíptico,  *x*  - e  *y*  -coordenadas de los puntos de control en el arco, ángulo desde el  *eje x*  al eje principal de la elipse y relación entre los ejes principales y los ejes menores de la elipse. 
  
Las filas EllipticalArcTo contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La coordenada  *x*  del vértice final de un arco.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Coordenada y* del vértice final de un arco.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |La coordenada  *x*  del punto de control del arco; un punto en el arco. El punto de control se encuentra mejor a medio camino entre los vértices inicial y final del arco. De lo contrario, el arco puede crecer hasta un tamaño extremo para pasar a través del punto de control, con resultados impredecibles.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordenada  *y*  del punto de control de un arco.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Ángulo del eje principal de un arco con relación al  *eje x*  de su elemento primario.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Relación entre el eje mayor y el eje menor de un arco. A pesar del significado normal de estas palabras, el eje "mayor" no tiene por qué ser más grande que el eje "menor", por lo que esta relación no tiene que ser mayor que 1. Si establece en esta celda un valor menor o igual que 0, o mayor que 1000, pueden producirse resultados inesperados.  <br/> |
   

