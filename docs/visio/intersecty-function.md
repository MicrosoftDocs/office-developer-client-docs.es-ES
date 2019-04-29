---
title: INTERSECTY (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Devuelve la coordenada y (en el sistema local de coordenadas) del punto donde se cortan dos líneas.
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426103"
---
# <a name="intersecty-function"></a>Función INTERSECTY

Devuelve la coordenada *y* (en el sistema local de coordenadas) del punto donde se cortan dos líneas. 
  
## <a name="syntax"></a>Sintaxis

INTERSECTX (* * *x1* * *, * * *Y1* * *, * * *angle1* * *, * * *x2* * *, * * *Y2* * *, * * *angle2* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _1_ <br/> |Obligatorio  <br/> |**Number** <br/> |Coordenada _x_de un punto de la primera recta.  <br/> |
| _a1_ <br/> |Obligatorio  <br/> |**Number** <br/> |Coordenada _y_de un punto de la primera recta.  <br/> |
| _angle1_ <br/> |Obligatorio  <br/> |**Number** <br/> | Valor de la celda Angle de la primera recta.  <br/> |
| _2x_ <br/> |Obligatorio  <br/> |**Number** <br/> |Coordenada _x_de un punto de la segunda recta.  <br/> |
| _Single_ <br/> |Obligatorio  <br/> |**Number** <br/> |Coordenada _y_de un punto de la segunda recta.  <br/> |
| _angle2_ <br/> |Obligatorio  <br/> |**Number** <br/> |Valor de la celda Angle de la segunda recta.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

Cada línea se define como un punto (*x,y*) y un ángulo. 
  
Microsoft Visio usa esta función en la celda PinY de una forma pegada a una guía girada. 
  
Si las rectas no se cruzan, la función devuelve un error de división por cero (#DIV/0!), aunque Visio lo pasa por alto y restaura el último valor conocido para este punto. 
  
## <a name="example"></a>Ejemplo

INTERSECTy (VertGuide! PinX, VertGuide! PinY, VertGuide! Angle, Guíahoriz! PinX, Guíahoriz! PinY, Guíahoriz! Respecto 
  
Devuelve la coordenada *y* del punto de intersección de VertGuide y guíahoriz en unidades de página. 
  

