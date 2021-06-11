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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411606"
---
# <a name="scratch-section"></a>Sección de borrador

Un área de trabajo para escribir y probar fórmulas a las que hacen referencia otras celdas.
  
## <a name="remarks"></a>Comentarios

Puede agregar esta sección con el cuadro de diálogo **Insertar sección**. Haga clic con el botón secundario en la ventana ShapeSheet y, a continuación, haga clic en **Insertar sección**.
  
La **sección Scratch** se usa normalmente para aislar cálculos complejos repetidos. Si la solución tiene un propósito bien definido, es más conveniente  usar una celda en la sección Celdas definidas por el usuario para mayor claridad, ya que las celdas de usuario se pueden nombrar. 
  
Las celdas de **la sección Scratch** usan unidades de dos maneras diferentes. Las celdas X e Y usan unidades de dibujo; Las celdas A a D no usan unidades. (En la jerga de los programadores C, las celdas X e Y se "escriben" y las celdas A a D son "void"). Las celdas **Scratch X** y **Scratch Y** suelen usarse para derivar coordenadas *x* e *y,* como **PinX** y **PinY,** o las celdas X e Y que se encuentran en una celda de sección **Geometría.** Las celdas de scratch A a D pueden mostrar las unidades que especifique. 
  
Una diferencia mayor es la manera en que dichas celdas almacenan los valores de puntos. Un punto de Visio es un único paquete de datos para una coordenada ( *x,y*). Cuando una fórmula devuelve un punto, su valor se puede interpretar de tres maneras, dependiendo de la celda ShapeSheet donde esté la fórmula. Las celdas que se relacionan con  *x*  -coordinates (por ejemplo, **PinX** o celdas de la columna X de una sección **Geometry)** extraen solo la  *parte x*  -coordinate de un valor de punto. Las celdas relacionadas  *con y*  -coordinates extraen solo la  *parte y*  -coordinate de un valor de punto. 
  
Por ejemplo, Visio extrae la fórmula `PNT(3,4)` de estas tres maneras. 
  
|**Cell**|**Si escribe**|**Visio la trata como**|**Resultado**|
|:-----|:-----|:-----|:-----|
| X  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 3,0000 pda.  <br/> |
| v  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4,0000 pda.  <br/> |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT(3.0000 in., 4.0000 in.)  <br/> |
   

