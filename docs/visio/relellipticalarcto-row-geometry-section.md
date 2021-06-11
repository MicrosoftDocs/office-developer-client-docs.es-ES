---
title: Fila RelEllipticalArcTo (sección Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Contiene las coordenadas x - e y del extremo de un arco elíptico con respecto al ancho y alto de la forma, x - e y -coordenadas de los puntos de control del arco con relación al ancho y alto de la forma, el ángulo desde el eje x hasta el eje principal de la elipse y la relación entre los ejes principales y los ejes menores de la elipse.
ms.openlocfilehash: e38f5f2baf6bb9ade31c2778799a3ece968147f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409100"
---
# <a name="relellipticalarcto-row-geometry-section"></a>Fila RelEllipticalArcTo (sección Geometría)

Contiene  *las*  coordenadas x - e  *y*  del extremo de un arco elíptico con respecto al ancho y alto de la forma,  *x*  - e  *y*  -coordenadas de los puntos de control del arco con relación al ancho y alto de la forma, el ángulo desde el  *eje x*  hasta el eje principal de la elipse y la relación entre los ejes principales y los ejes menores de la elipse. 
  
> [!NOTE]
> Una **fila RelEllipticalArcTo** solo se puede conservar en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm. Cuando se guarda un archivo en los formatos Visio 2003-2010, la fila **RelEllipticalArcTo** se convierte en una fila [EllipticalArcTo.](ellipticalarcto-row-geometry-section.md) 
  
Una **fila RelEllipticalArcTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La coordenada  *x*  del vértice final de un arco con relación al ancho de la forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordenada  *y*  del vértice final de un arco con relación al alto de la forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |La coordenada  *x*  del punto de control del arco con relación al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor a medio camino entre los vértices inicial y final del arco. De lo contrario, el arco puede crecer hasta un tamaño extremo para pasar a través del punto de control, con resultados impredecibles.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordenada  *y*  del punto de control de un arco con relación al ancho de la forma.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Ángulo del eje principal de un arco con relación al  *eje x*  de su elemento primario.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Relación entre el eje mayor y el eje menor de un arco. A pesar del significado normal de estas palabras, el eje "mayor" no tiene por qué ser más grande que el eje "menor", por lo que esta relación no tiene que ser mayor que 1. Si establece en esta celda un valor menor o igual que 0, o mayor que 1000, pueden producirse resultados inesperados.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores de la **fila RelEllipticalArcTo** son equivalentes a los valores de una fila [EllipticalArcTo,](ellipticalarcto-row-geometry-section.md) multiplicados por el ancho y el alto de la forma. Por ejemplo: una fila **RelEllipticalArcTo** donde las celdas **X**, **Y**, **A**, **B,** **C** y **D** tienen los valores 1, 1, 1,5, 0,5, 15 deg y 1,5 (respectivamente) se pueden reemplazar por una fila **EllipticalArcTo** con las fórmulas de celda  `Width*1` , , , ,  `Height*1'`  `Width*1.5`  `Height*0.5` 15 deg y 1,5 (respectivamente).
  

