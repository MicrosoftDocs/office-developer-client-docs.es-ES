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
  
Las celdas de ShapeSheet de Microsoft Visio contienen valores y fórmulas. A su vez, las fórmulas pueden tener referencias a otras celdas, lo que le da la capacidad de calcular un valor en una celda basándose en el valor de otra celda. Sin embargo, al crear o mantener formas complejas, puede resultar difícil identificar todas estas interdependencias, dado que una fórmula puede hacer referencia a cualquier celda del dibujo, sea una celda de la misma ShapeSheet o de otro objeto del dibujo (por ejemplo, una página, un estilo, un patrón u otra forma). 
  
La **ventana Seguimiento de** fórmulas proporciona información que le ayudará a comprender las implicaciones de los cambios realizados en las celdas. 
  
## <a name="displaying-the-formula-tracing-window"></a>Mostrar la ventana Seguimiento de fórmulas

Para ver la ventana **Seguimiento** de fórmulas, con la ventana ShapeSheet activa, en Herramientas de **ShapeSheet** en la ficha ** Diseño **, en el grupo Seguimiento de **fórmulas,** haga clic en **Mostrar ventana**. La  ventana Seguimiento de fórmulas aparece acoplada en la ventana ShapeSheet de forma predeterminada, pero es una ventana anclada que  se puede acoplar, flotar o combinar con otras ventanas ShapeSheet ancladas disponibles, por ejemplo, la ventana Explorador de estilos. 
  
## <a name="tracing-dependent-cells"></a>Rastreo de celdas dependientes

Para ver una lista de las celdas dependientes de una celda determinada, seleccione dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Width. 
  
![La celda Width está seleccionada](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Para ver sus celdas dependientes, en el grupo **Seguimiento de** fórmulas, haga clic en **Seguimiento dependientes**.
  
Aparecerá una lista de todas las celdas que dependan de Width en la ventana **Rastreo de fórmulas**. Puede explorar cualquiera de ellas haciendo doble clic en la ventana **Rastreo de fórmulas**. 
  
![Todas las celdas con una dependencia en la celda Width aparecen en la ventana Seguimiento de fórmulas](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>Seguimiento de celdas precendentes

Para ver una lista de las celdas de las cuales depende una celda determinada, seleccione primero dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Geometry1.X2. 
  
![La celda Geometry1.X2 está seleccionada](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Para ver las celdas precedentes, en el grupo **Seguimiento de** fórmulas, haga clic en **Seguir precedentes**.
  
En la ventana Seguimiento de fórmulas aparece una lista de  todas las celdas de las que depende la celda Geometry1.X2. Puede explorar cualquiera de ellas haciendo doble clic en la ventana **Rastreo de fórmulas**. 
  
![Todas las celdas de las que depende la celda Geometry1.X2 aparecen en la ventana Seguimiento de fórmulas](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

