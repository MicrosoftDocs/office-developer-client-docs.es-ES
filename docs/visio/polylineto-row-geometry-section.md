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
description: Contiene x - e y-coordenadas del último punto de una polilínea y una fórmula de polilínea.
ms.openlocfilehash: 56cecb2eeaa1702461b1096fe468974f2f0b1f52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822765"
---
# <a name="polylineto-row-geometry-section"></a>Fila PolylineTo (sección Geometría)

Contiene *x* - e *y* -coordenadas del último punto de una polilínea y una fórmula de polilínea. 
  
Las filas PolylineTo contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La *x* -coordenadas del vértice del extremo de una polilínea.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La *y* -coordenadas del vértice del extremo de una polilínea.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Fórmula de polilínea.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las líneas representadas por filas Polyline son equivalentes a las representadas por una secuencia de filas LineTo, pero la fila Polyline es más eficaz. Puede cambiar una fila PolylineTo por una fila LineTo para poder ver fácilmente la geometría de la forma. Para ello, haga clic con el botón secundario del mouse (ratón) en la fila PolylineTo y, a continuación, haga clic en Expandir fila en el menú contextual. 
  
Para cambiar un tipo de fila por una fila PolylineTo, haga clic con el botón secundario del mouse en la fila y, a continuación, haga clic en Cambiar tipo de fila en el menú contextual. 
  

