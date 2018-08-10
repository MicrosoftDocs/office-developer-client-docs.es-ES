---
title: Fila ArcTo (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Contiene x - e y-las coordenadas y la curvatura de un arco circular.
ms.openlocfilehash: 77ed0dcaee7ddefa8771d3e890776d4adfcc3b40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821536"
---
# <a name="arcto-row-geometry-section"></a>Fila ArcTo (sección Geometría)

Contiene el *x* - e *y* -las coordenadas y la curvatura de un arco circular. 
  
Las filas ArcTo contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La *x* -coordenadas del vértice del extremo de un arco.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La *y* -coordenadas del vértice del extremo de un arco.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Distancia desde el punto medio del arco hasta el punto medio de su cuerda.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los arcos que dibuja Visio son elípticos, incluso si se basan en un círculo. De forma predeterminada, los arcos dibujados se representan mediante una fila EllipticalArcTo en la ventana ShapeSheet. Para mostrar una fila ArcTo en una ventana ShapeSheet, tiene que dibujar un arco y, a continuación, cambiar el tipo de fila EllipticalArcTo por el tipo ArcTo; en efecto, está cambiando un arco elíptico por un arco circular.
  
Para cambiar un tipo de fila, haga clic con el botón secundario del mouse (ratón) en la fila y, a continuación, haga clic en Cambiar tipo de fila en el menú contextual. 
  

