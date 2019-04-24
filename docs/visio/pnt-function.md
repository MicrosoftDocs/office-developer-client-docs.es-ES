---
title: PNT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Devuelve el punto representado por las coordenadas x e y como un valor único.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322354"
---
# <a name="pnt-function"></a>Función PNT

Devuelve el punto representado por las coordenadas _x_ e __ y como un valor único. 
  
## <a name="syntax"></a>Sintaxis

PNT (* * *x, y* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _x, y_ <br/> |Obligatorio  <br/> |**Number, Number** <br/> |Coordenadas del punto en el sistema de coordenadas de la forma actual.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Point
  
## <a name="remarks"></a>Comentarios

La conversión de coordenadas a puntos le permite cambiar la geometría de una forma sin tener que manipular las coordenadas *x* -e *y* -por separado. 
  
## <a name="example"></a>Ejemplo

PNT (PinX, PinY) 
  
Devuelve el punto representado por las coordenadas PinX y PinY. 
  

