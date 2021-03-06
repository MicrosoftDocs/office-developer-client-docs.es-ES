---
title: Fila PolylineTo (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: Contiene las coordenadas x - e y del último punto de una polilínea y una fórmula de polilínea.
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439467"
---
# <a name="polylineto-row-geometry-section"></a>Fila PolylineTo (Sección de Geometría)

Contiene  *las coordenadas x*  - e  *y*  del último punto de una polilínea y una fórmula de polilínea. 
  
Las filas PolylineTo contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La coordenada  *x*  del vértice final de una polilínea.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Coordenada y* del vértice final de una polilínea.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Fórmula de polilínea.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las líneas representadas como fila Polyline son equivalentes a las líneas representadas como una secuencia de filas LineTo, pero una fila Polyline es más eficiente. Puede cambiar una fila PolylineTo a una fila LineTo para que pueda ver fácilmente la geometría de la forma. Para ello, haga clic con el botón secundario en la fila PolylineTo y, a continuación, haga clic **en Expandir fila** en el menú contextual. 
  
Para cambiar un tipo de fila a una fila PolylineTo, haga clic con el botón secundario en la fila y, a continuación, haga clic en **Cambiar** tipo de fila en el menú contextual. 
  

