---
title: INTERSECTX (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
localization_priority: Normal
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: Devuelve la coordenada x (en el sistema de coordenadas local) del punto donde se cruzan dos líneas.
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418277"
---
# <a name="intersectx-function"></a>Función INTERSECTX

Devuelve la coordenada  *x*  (en el sistema de coordenadas local) del punto donde se cruzan dos líneas. 
  
## <a name="syntax"></a>Sintaxis

INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Obligatorio  <br/> |**Number** <br/> |La coordenada  _x_ de un punto en la primera línea.  <br/> |
| _y1_ <br/> |Obligatorio  <br/> |**Number** <br/> |Coordenada  _y_ de un punto en la primera línea.  <br/> |
| _angle1_ <br/> |Obligatorio  <br/> |**Number** <br/> | Valor de la celda Angle de la primera recta.  <br/> |
| _x2_ <br/> |Obligatorio  <br/> |**Number** <br/> |La coordenada  _x_ de un punto en la segunda línea.  <br/> |
| _y2_ <br/> |Obligatorio  <br/> |**Number** <br/> |Coordenada  _y_ de un punto en la segunda línea.  <br/> |
| _angle2_ <br/> |Obligatorio  <br/> |**Number** <br/> |Valor de la celda Angle de la segunda recta.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

Cada línea se define como un punto (*x,y*) y un ángulo. 
  
Microsoft Visio usa esta función en la celda PinX de una forma pegada a una guía girada. 
  
Si las rectas no se cruzan, la función devuelve un error de división por cero (#DIV/0!), aunque Visio lo pasa por alto y restaura el último valor conocido para este punto. 
  
## <a name="example"></a>Ejemplo

INTERSECTX(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide! PinX,HorzGuide! PinY,HorzGuide! Ángulo) 
  
Devuelve la coordenada  *x*  del punto de intersección de VertGuide y HorzGuide en las unidades de página. 
  

