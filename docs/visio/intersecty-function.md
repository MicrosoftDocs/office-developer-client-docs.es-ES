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
description: Devuelve la coordenada y (en el sistema de coordenadas local) del punto en el que se cruzan dos líneas.
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426103"
---
# <a name="intersecty-function"></a>Función INTERSECTY

Devuelve la  *coordenada y*  (en el sistema de coordenadas local) del punto en el que se cruzan dos líneas. 
  
## <a name="syntax"></a>Sintaxis

INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Obligatorio  <br/> |**Number** <br/> |Coordenada  _x_ de un punto de la primera línea.  <br/> |
| _y1_ <br/> |Obligatorio  <br/> |**Number** <br/> |Coordenada  _y_ de un punto de la primera línea.  <br/> |
| _angle1_ <br/> |Obligatorio  <br/> |**Number** <br/> | Valor de la celda Angle de la primera recta.  <br/> |
| _x2_ <br/> |Obligatorio  <br/> |**Number** <br/> |Coordenada  _x_ de un punto de la segunda línea.  <br/> |
| _y2_ <br/> |Obligatorio  <br/> |**Number** <br/> |Coordenada  _y_ de un punto de la segunda línea.  <br/> |
| _angle2_ <br/> |Obligatorio  <br/> |**Number** <br/> |Valor de la celda Angle de la segunda recta.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

Cada línea se define como un punto (*x,y*) y un ángulo. 
  
Microsoft Visio usa esta función en la celda PinY de una forma pegada a una guía girada. 
  
Si las rectas no se cruzan, la función devuelve un error de división por cero (#DIV/0!), aunque Visio lo pasa por alto y restaura el último valor conocido para este punto. 
  
## <a name="example"></a>Ejemplo

INTERSECTY(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide! PinX,HorzGuide! PinY,HorzGuide! Ángulo) 
  
Devuelve la  *coordenada y*  del punto de intersección de VertGuide y HorzGuide en unidades de página. 
  

