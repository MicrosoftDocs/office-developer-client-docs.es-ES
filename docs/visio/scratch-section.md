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
ms.openlocfilehash: 16f0bac8f139c0b03d7826ac377a964d15296dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823107"
---
# <a name="scratch-section"></a>Sección Borrador

Un área de trabajo para escribir y probar fórmulas a las que hacen referencia otras celdas.
  
## <a name="remarks"></a>Observaciones

Puede agregar esta sección con el cuadro de diálogo **Insertar sección**. Haga clic con el botón secundario en la ventana ShapeSheet y, a continuación, haga clic en **Insertar sección**.
  
La sección **de borrador** se usa normalmente para aislar cálculos complejos que se repiten. Si su solución tiene un propósito bien definido, es mejor utilizar una celda de la sección **User-Defined Cells** para mayor claridad, debido a que las celdas de usuario pueden tener nombre. 
  
Las celdas en la sección **de borrador** utilizan unidades de dos maneras diferentes. Las celdas X e Y utilizan unidades de dibujo; Un a celdas D no utiliza unidades. (En Scratch, las celdas X e Y se "ha escrito", y las celdas de la A la D son "void".) Las celdas Scratch **X** y **Scratch Y** a menudo se usan para derivar coordenadas *x* e *y* , como **PinX** y **PinY**o las celdas X e Y que se encuentra en una celda de la sección de **geometría** . Scratch celdas a la D puede mostrar cualquier unidad que especifique. 
  
Una diferencia mayor es la manera en que dichas celdas almacenan los valores de punto. Un punto en Visio es un paquete de datos para una coordenada ( *x, y*). Cuando una fórmula devuelve un valor de punto, ese valor se interpreta en uno de tres maneras, dependiendo de la celda ShapeSheet en que la fórmula es. Las celdas que se relacionan con *x* -coordenadas (por ejemplo, **PinX**o las celdas de la columna X de una sección de **geometría** ) extracción sólo la *x* -coordinar parte de un valor en puntos. Las celdas que se relacionan con *y* -coordenadas extracción sólo la *y* -coordinar parte de un valor en puntos. 
  
Por ejemplo, Visio extrae la fórmula `PNT(3,4)` de estas tres maneras. 
  
|**Cell**|**Si escribe**|**Visio la trata como**|**Resultado**|
|:-----|:-----|:-----|:-----|
| X  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | 3,0000 pda.  <br/> |
| Y  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | 4,0000 pda.  <br/> |
| A-D  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | PNT (3,0000 pda., 4,0000 pda.)  <br/> |
   

