---
title: Ventana Rastreo de fórmulas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
localization_priority: Normal
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: La ventana Rastreo de fórmulas se ha diseñado para ofrecer a los programadores de formas información sobre las interdependencias entre celdas, tanto las dependientes (celdas que dependen de otra celda determinada) como las precedentes (celdas de las cuales depende una celda determinada).
ms.openlocfilehash: f5f9d6a7ba3ab7049715d31342cfe7aa68ea053f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345335"
---
# <a name="about-the-formula-tracing-window"></a>Acerca de la ventana Rastreo de fórmulas

La ventana **Rastreo de fórmulas** se ha diseñado para ofrecer a los programadores de formas información sobre las interdependencias entre celdas, tanto las dependientes (celdas que dependen de otra celda determinada) como las precedentes (celdas de las cuales depende una celda determinada). 
  
Las celdas de ShapeSheet de Microsoft Visio contienen valores y fórmulas. Las fórmulas, a su vez, tienen referencias a otras celdas, lo que le permite calcular un valor en una celda basándose en el valor de otra celda. Sin embargo, al crear o mantener formas complejas, puede resultar difícil identificar todas estas interdependencias, dado que una fórmula puede hacer referencia a cualquier celda del dibujo, sea una celda de la misma ShapeSheet o de otro objeto del dibujo (por ejemplo, una página, un estilo, un patrón u otra forma). 
  
La **** ventana Rastreo de fórmulas proporciona información que le ayudará a comprender las consecuencias de los cambios que realice en las celdas. 
  
## <a name="displaying-the-formula-tracing-window"></a>Mostrar la ventana Rastreo de fórmulas

Para ver la **** ventana Rastreo de fórmulas, con la ventana ShapeSheet activa, en **herramientas de ShapeSheet** en la ficha * * Diseño * *, en el grupo **seguimiento** de fórmulas, haga clic en **Mostrar ventana**. La **** ventana Rastreo de fórmulas aparece acoplada de forma predeterminada a la ventana ShapeSheet, pero es una ventana anclada que puede acoplarse, flotar o fusionarse con otras ventanas de ShapeSheet disponibles, por ejemplo, la ventana **Explorador de estilos** . 
  
## <a name="tracing-dependent-cells"></a>Rastreo de celdas dependientes

Para ver una lista de las celdas dependientes de una celda determinada, seleccione dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Width. 
  
![La celda width está seleccionada](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Para ver las celdas dependientes, en el grupo **seguimiento**de fórmulas, haga clic en **rastrear**dependientes.
  
Aparecerá una lista de todas las celdas que dependan de Width en la ventana **Rastreo de fórmulas**. Puede explorar cualquiera de ellas haciendo doble clic en la ventana **Rastreo de fórmulas**. 
  
![Todas las celdas con una dependencia en la celda width aparecen en la ventana Rastreo de fórmulas.](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>Seguimiento de celdas de precendent

Para ver una lista de las celdas de las cuales depende una celda determinada, seleccione primero dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Geometry1.X2. 
  
![La celda Geometry1. x2 está seleccionada](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Para ver sus celdas precedentes, en el grupo **seguimiento**de fórmulas, haga clic en **Rastrear precedentes**.
  
Aparece una lista de todas las celdas de las que depende la celda Geometry1. x2 en la **** ventana Rastreo de fórmulas. Puede explorar cualquiera de ellas haciendo doble clic en la ventana **Rastreo de fórmulas**. 
  
![Todas las celdas en las que depende la celda Geometry1. x2 aparecen en la ventana Rastreo de fórmulas](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

