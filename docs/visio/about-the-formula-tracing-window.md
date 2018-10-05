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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385329"
---
# <a name="about-the-formula-tracing-window"></a>Información sobre la ventana Rastreo de fórmulas

La ventana **Rastreo de fórmulas** se ha diseñado para ofrecer a los programadores de formas información sobre las interdependencias entre celdas, tanto las dependientes (celdas que dependen de otra celda determinada) como las precedentes (celdas de las cuales depende una celda determinada). 
  
Las celdas de ShapeSheet de Microsoft Visio contienen valores y fórmulas. Fórmulas a su vez, pueden hacer que las referencias a otras celdas, que ofrece la potencia para calcular un valor en una celda basándose en el valor de otra celda. Al crear o mantener formas complejas, sin embargo, puede resultar difícil identificar todas estas interdependencias debido a que una fórmula puede hacer referencia a cualquier celda del dibujo, ya sea una celda de la misma ShapeSheet o una celda perteneciente a otro objeto en el dibujo, Por ejemplo, una página, estilo, patrón u otra forma. 
  
La ventana **Rastreo de fórmulas** ofrece información para ayudarle a comprender las consecuencias de los cambios realizados a las celdas. 
  
## <a name="displaying-the-formula-tracing-window"></a>Mostrar la ventana Rastreo de fórmulas

Para ver la ventana **Rastreo de fórmulas** , con la ventana ShapeSheet activa, en **Herramientas de ShapeSheet** en la ** diseño ** ficha, en el grupo **Rastreo de fórmulas** , haga clic en **Mostrar ventana**. La ventana **Rastreo de fórmulas** aparece acoplada en la ventana ShapeSheet de forma predeterminada, pero es una ventana anclada que puede acoplar, flotar o combinada con otras ventanas de ShapeSheet disponibles, por ejemplo, la ventana **Explorador de estilos** . 
  
## <a name="tracing-dependent-cells"></a>Rastreo de celdas dependientes

Para ver una lista de las celdas dependientes de una celda determinada, seleccione dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Width. 
  
![Se selecciona la celda Width](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Para ver sus celdas dependientes, en el grupo **Rastreo de fórmulas**, haga clic en **Rastrear dependientes**.
  
Aparecerá una lista de todas las celdas que dependan de Width en la ventana **Rastreo de fórmulas**. Puede explorar cualquiera de ellas haciendo doble clic en la ventana **Rastreo de fórmulas**. 
  
![Todas las celdas con una dependencia en la celda Width aparecen en la ventana Rastreo de fórmulas](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>Rastreo de celdas precendent

Para ver una lista de las celdas de las cuales depende una celda determinada, seleccione primero dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Geometry1.X2. 
  
![Se selecciona la celda Geometry1.X2](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Para ver sus celdas precedentes, en el grupo **Rastreo de fórmulas**, haga clic en **Rastrear precedentes**.
  
Aparece una lista de todas las celdas que depende la celda Geometry1.X2 en la ventana **Rastreo de fórmulas** . Puede navegar a cualquier celda de la lista haciendo doble clic en su entrada en la ventana **Rastreo de fórmulas** . 
  
![Todas las celdas que depende la celda Geometry1.X2 aparecen en la ventana Rastreo de fórmulas](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

