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
description: La ventana Rastreo de fórmulas está diseñada para proporcionar a los programadores de forma con información acerca de las interdependencias entre celdas, celdas dependientes (celdas que tengan una dependencia en una celda determinada) y las celdas precedentes (celdas que depende de una celda determinada).
ms.openlocfilehash: 316ac219f548b2459ea2d0ad8cece0f693957fcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821492"
---
# <a name="about-the-formula-tracing-window"></a>Ventana Rastreo de fórmulas

La ventana **Rastreo de fórmulas** está diseñada para proporcionar a los programadores de forma con información acerca de las interdependencias entre celdas, celdas dependientes (celdas que tengan una dependencia en una celda determinada) y las celdas precedentes (celdas que depende de una celda determinada). 
  
Las celdas de ShapeSheet de Microsoft Visio contienen valores y fórmulas. Fórmulas a su vez, pueden hacer que las referencias a otras celdas, que ofrece la potencia para calcular un valor en una celda basándose en el valor de otra celda. Al crear o mantener formas complejas, sin embargo, puede resultar difícil identificar todas estas interdependencias debido a que una fórmula puede hacer referencia a cualquier celda del dibujo, ya sea una celda de la misma ShapeSheet o una celda perteneciente a otro objeto en el dibujo, Por ejemplo, una página, estilo, patrón u otra forma. 
  
La ventana **Rastreo de fórmulas** ofrece información para ayudarle a comprender las consecuencias de los cambios realizados a las celdas. 
  
## <a name="displaying-the-formula-tracing-window"></a>Mostrar la ventana Rastreo de fórmulas

Para ver la ventana **Rastreo de fórmulas** , con la ventana ShapeSheet activa, en **Herramientas de ShapeSheet** en la ** diseño ** ficha, en el grupo **Rastreo de fórmulas** , haga clic en **Mostrar ventana**. La ventana **Rastreo de fórmulas** aparece acoplada en la ventana ShapeSheet de forma predeterminada, pero es una ventana anclada que puede acoplar, flotar o combinada con otras ventanas de ShapeSheet disponibles, por ejemplo, la ventana **Explorador de estilos** . 
  
## <a name="tracing-dependent-cells"></a>Rastreo de celdas dependientes

Para ver una lista de las celdas dependientes de una celda determinada, seleccione dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Width. 
  
![](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
Para ver sus celdas dependientes, en el grupo **Rastreo de fórmulas**, haga clic en **Rastrear dependientes**.
  
Aparece una lista de todas las celdas con una dependencia en la celda Width en la ventana **Rastreo de fórmulas** . Puede navegar a cualquier celda de la lista haciendo doble clic en su entrada en la ventana **Rastreo de fórmulas** . 
  
![](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a>Rastreo de celdas precendent

Para ver una lista de las celdas de las cuales depende una celda determinada, seleccione primero dicha celda en la ventana ShapeSheet. En este ejemplo, está seleccionada la celda Geometry1.X2. 
  
![](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
Para ver sus celdas precedentes, en el grupo **Rastreo de fórmulas**, haga clic en **Rastrear precedentes**.
  
Aparece una lista de todas las celdas que depende la celda Geometry1.X2 en la ventana **Rastreo de fórmulas** . Puede navegar a cualquier celda de la lista haciendo doble clic en su entrada en la ventana **Rastreo de fórmulas** . 
  
![](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

