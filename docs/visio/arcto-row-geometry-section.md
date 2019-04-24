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
description: Contiene las coordenadas x e y y la curvatura de un arco circular.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341408"
---
# <a name="arcto-row-geometry-section"></a>Fila ArcTo (Sección de geometría)

Contiene las coordenadas *x* e ** y y la curvatura de un arco circular. 
  
Las filas ArcTo contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordenada *x* del vértice del extremo de un arco.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordenada *y* del vértice del extremo de un arco.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Distancia desde el punto medio del arco hasta el punto medio de su cuerda.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los arcos que dibuja Visio son elípticos, incluso si se basan en un círculo. De forma predeterminada, los arcos dibujados se representan mediante una fila EllipticalArcTo en la ventana ShapeSheet. Para mostrar una fila ArcTo en una ventana ShapeSheet, tiene que dibujar un arco y, a continuación, cambiar el tipo de fila EllipticalArcTo por el tipo ArcTo; en efecto, está cambiando un arco elíptico por un arco circular.
  
Para cambiar un tipo de fila, haga clic con el botón secundario en una fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual. 
  

