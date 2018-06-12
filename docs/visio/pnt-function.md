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
ms.openlocfilehash: be00f7d5ae55f70407e35eca43881a6d3f70ec13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822819"
---
# <a name="pnt-function"></a>PNT (función)

Devuelve el punto representado por las coordenadas _x_ e _y_ como un valor único. 
  
## <a name="syntax"></a>Sintaxis

PNT (** *x, y* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _x, y_ <br/> |Obligatorio  <br/> |**Número, número** <br/> |Coordenadas del punto en el sistema de coordenadas de la forma actual.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Punto
  
## <a name="remarks"></a>Observaciones

Convertir las coordenadas en puntos permite cambiar la geometría de una forma sin tener que manipular *x* e *y* -coordina por separado. 
  
## <a name="example"></a>Ejemplo

PNT(PinX,PinY) 
  
Devuelve el punto representado por las coordenadas PinX y PinY. 
  

