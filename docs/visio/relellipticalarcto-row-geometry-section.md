---
title: Fila RelEllipticalArcTo (sección Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Contiene x - y y - coordenadas del extremo de un arco elíptico con relación al ancho de la forma y height, x - e y-las coordenadas de los puntos de control del arco con respecto al ancho de la forma y el alto, ángulo desde la x-eje al eje de la elipse y la relación entre t principales y secundarias ejes de la elipse.
ms.openlocfilehash: 417a2a92bc5c94f9620c7c6f1081ba81d93aa890
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822939"
---
# <a name="relellipticalarcto-row-geometry-section"></a>Fila RelEllipticalArcTo (sección Geometría)

Contiene *x* - y *y* - coordenadas del extremo de un arco elíptico con relación al ancho de la forma y height, *x* - e *y* -las coordenadas de los puntos de control del arco con respecto al ancho de la forma y el alto, ángulo desde *x*   -eje al eje de la elipse y la relación entre los ejes mayor y menor de la elipse. 
  
> [!NOTE]
> Una fila de **RelEllipticalArcTo** sólo puede persistir en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm. Cuando se guarda un archivo a los formatos de Visio 2003 2010, la fila de **RelEllipticalArcTo** se convierte en una fila [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) . 
  
Una fila de **RelEllipticalArcTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La *x* -coordenadas del vértice del extremo de un arco en relación con el ancho de la forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La *y* -coordenadas del vértice del extremo de un arco con relación al alto de la forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |La *x* -coordenadas del punto de control del arco con respecto al ancho de la forma; un punto en el arco. El punto de control es mejor encuentra acerca de la mitad de la distancia entre el principio y el vértice final del arco. De lo contrario, el arco puede crecer demasiado para pasar por el punto de control, con resultados impredecibles.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |La *y* -coordenadas del punto de control de un arco con respecto al ancho de la forma.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Ángulo del eje mayor de un arco con respecto a la *x* -eje de su forma principal.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Relación entre el eje mayor y el eje menor de un arco. A pesar del significado normal de estas palabras, el eje "mayor" no tiene por qué ser más grande que el eje "menor", por lo que esta relación no tiene que ser mayor que 1. Si establece en esta celda un valor menor o igual que 0, o mayor que 1000, pueden producirse resultados inesperados.  <br/> |
   
## <a name="remarks"></a>Comentarios

Valores de la fila de **RelEllipticalArcTo** son equivalentes a los valores de una fila [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) , multiplicado por el ancho y el alto de la forma. Por ejemplo: un **RelEllipticalArcTo** fila donde las celdas **X**, **Y**, **A**, **B**, **C**y **D** tienen los valores 1, 1, 1,5, 0,5, 15 grad y 1,5 (respectivamente) que se pueden reemplazar con una fila **EllipticalArcTo** con las fórmulas de celda `Width*1`, `Height*1'`, `Width*1.5`, `Height*0.5`, 15 grad y 1,5 (respectivamente).
  

