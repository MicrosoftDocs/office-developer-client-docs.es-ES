---
title: Sección de borrador
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
localization_priority: Normal
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: Un área de trabajo para escribir y probar fórmulas a las que hacen referencia otras celdas.
ms.openlocfilehash: a7d2c6762e96fc19986521c2ba164666b925c928
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344530"
---
# <a name="scratch-section"></a>Sección de borrador

Un área de trabajo para escribir y probar fórmulas a las que hacen referencia otras celdas.
  
## <a name="remarks"></a>Comentarios

Puede agregar esta sección con el cuadro de diálogo **Insertar sección**. Haga clic con el botón secundario en la ventana ShapeSheet y, a continuación, haga clic en **Insertar sección**.
  
La **** sección de borrador suele usarse para aislar cálculos complejos repetidos. Si la solución tiene un propósito bien definido, es Wiser usar una celda de la sección de **celdas definidas por el usuario** para lograr una mayor claridad porque se pueden asignar nombres a las celdas de usuario. 
  
Las celdas de la sección **Scratch** usan unidades de dos maneras diferentes. Las celdas X e y usan unidades de dibujo; Las celdas de la a a la D no usan unidades. (En la jerga de los programadores de C, las celdas X e y se "escriben" y las celdas de la a a la D son "Void".) Las **celdas Scratch x** y **Scratch** y se suelen usar para derivar coordenadas *x* e ** y, como **PinX** y **PinY**, o las celdas x e y que se encuentran en una celda de la sección **Geometry** . Las celdas de grietas de la a a la D pueden mostrar las unidades que especifique. 
  
Una diferencia mayor es la manera en que dichas celdas almacenan los valores de puntos. Un punto en Visio es un paquete de datos único para una coordenada ( *x, y*). Cuando una fórmula devuelve un punto, su valor se puede interpretar de tres maneras, dependiendo de la celda ShapeSheet donde esté la fórmula. Las celdas relacionadas con las coordenadas *x* (por ejemplo, **PinX**o las celdas de la columna x de una sección **Geometry** ) extraen sólo la parte *x* -coordinada de un valor Point. Las celdas relacionadas con las coordenadas *y* extraen sólo la parte de coordenada *y* de un valor de punto. 
  
Por ejemplo, Visio extrae la `PNT(3,4)` fórmula de estas tres formas. 
  
|**Cell**|**Si escribe**|**Visio la trata como**|**Resultado**|
|:-----|:-----|:-----|:-----|
| X  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 3,0000 pda.  <br/> |
| v  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4,0000 pda.  <br/> |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT (3.0000 in., 4,0000)  <br/> |
   

