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
description: Devuelve la x-coordenada (en el sistema de coordenadas local) del punto donde se cortan dos líneas.
ms.openlocfilehash: ea5a08f25f3e45dab3fe3fd83b74cf9a7541b6e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822342"
---
# <a name="intersectx-function"></a>Función INTERSECTX

Devuelve la *x* -coordenada (en el sistema de coordenadas local) del punto donde se cortan dos líneas. 
  
## <a name="syntax"></a>Sintaxis

INTERSECTX (** *x1* **, ** *y1* **, ** *ángulo1* **, ** *x2* **, ** *y2* **, ** *ángulo2* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _X1_ <br/> |Obligatorio  <br/> |**Número** <br/> |La _x_-coordenadas de un punto de la primera línea.  <br/> |
| _Y1_ <br/> |Obligatorio  <br/> |**Número** <br/> |La _y_-coordenadas de un punto de la primera línea.  <br/> |
| _ángulo1_ <br/> |Obligatorio  <br/> |**Número** <br/> | Valor de la celda Angle de la primera recta.  <br/> |
| _X2_ <br/> |Obligatorio  <br/> |**Número** <br/> |La _x_-coordenadas de un punto de la segunda recta.  <br/> |
| _y2_ <br/> |Obligatorio  <br/> |**Número** <br/> |La _y_-coordenadas de un punto de la segunda recta.  <br/> |
| _ángulo2_ <br/> |Obligatorio  <br/> |**Número** <br/> |Valor de la celda Angle de la segunda recta.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Number
  
## <a name="remarks"></a>Comentarios

Cada línea se define como un punto (*x,y*) y un ángulo. 
  
Microsoft Visio usa esta función en la celda PinX de una forma pegada a una guía girada. 
  
Si las rectas no se cruzan, la función devuelve un error de división por cero (#DIV/0!), aunque Visio lo pasa por alto y restaura el último valor conocido para este punto. 
  
## <a name="example"></a>Ejemplo

¡INTERSECTX (VertGuide! ¡PinX, VertGuide! PinY, VertGuide! ¡GuíaVertical! ¡PinX, GuíaHoriz! PinY, GuíaHoriz! Ángulo) 
  
Devuelve la *x* -coordenadas del punto donde se cortan GuíaVertical y GuíaHoriz en unidades de página. 
  

