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
description: Contiene las coordenadas x e y del último punto de una polilínea y una fórmula de polilínea.
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359832"
---
# <a name="polylineto-row-geometry-section"></a>Fila PolylineTo (Sección de Geometría)

Contiene las coordenadas *x* e y del último punto de una polilínea y una fórmula de polilínea. ** 
  
Las filas PolylineTo contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordenada *x* del vértice del extremo de una polilínea.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordenada *y* del vértice del extremo de una polilínea.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Fórmula de polilínea.  <br/> |
   
## <a name="remarks"></a>Comentarios

Las líneas representadas como fila Polyline son equivalentes a las líneas representadas como una secuencia de filas lineTo, pero la fila Polyline es más eficaz. Puede cambiar una fila PolylineTo a una fila lineTo para que pueda ver fácilmente la geometría de forma. Para ello, haga clic con el botón secundario en la fila PolylineTo y, a continuación, haga clic en **expandir fila** en el menú contextual. 
  
Para cambiar un tipo de fila a una fila PolylineTo, haga clic con el botón secundario en la fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual. 
  

