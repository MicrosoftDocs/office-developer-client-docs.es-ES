---
title: HSL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
localization_priority: Normal
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Devuelve un valor que representa un índice en la paleta de colores del documento. Especifica un color por su matiz, saturación y componentes de luminosidad.
ms.openlocfilehash: 50f343d990157d831ac4ac43057d0a2b7fca63f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822297"
---
# <a name="hsl-function"></a>HSL (función)

Devuelve un valor que representa un índice en la paleta de colores del documento. Especifica un color por su matiz, saturación y componentes de luminosidad.
  
## <a name="syntax"></a>Sintaxis

HSL (** *matiz* **, ** *saturación* **, ** *luminosidad* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _matiz_ <br/> |Obligatorio  <br/> |**Número** <br/> |El matiz del color, expresado como un número comprendido entre 0 y 239, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.  <br/> |
| _saturación_ <br/> |Obligatorio  <br/> |**Número** <br/> |La saturación del color, expresada como un número comprendido entre 0 y 240, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.  <br/> |
| _luminosidad_ <br/> |Obligatorio  <br/> |**Número** <br/> | La luminosidad del color, expresada como un número comprendido entre 0 y 240, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Number
  
## <a name="remarks"></a>Observaciones

Si el color que devuelve la función no forma parte de la paleta de colores del documento actual, se agregará a la lista de colores disponibles del documento. 
  
La tabla siguiente muestra varios colores estándar y los valores correspondientes al matiz, saturación y luminosidad. 
  
|**Color**|**Valor de matiz**|**Valor de saturación**|**Valor de luminosidad**|
|:-----|:-----|:-----|:-----|
|Negro  <br/> |0  <br/> |0  <br/> |24  <br/> |
|Azul  <br/> |160  <br/> |240  <br/> |120  <br/> |
|Verde  <br/> |80  <br/> |240  <br/> |120  <br/> |
|Cian  <br/> |120  <br/> |240  <br/> |120  <br/> |
|Rojo  <br/> |0  <br/> |240  <br/> |120  <br/> |
|Magenta  <br/> |200  <br/> |240  <br/> |120  <br/> |
|Amarillo  <br/> |40  <br/> |240  <br/> |120  <br/> |
|Blanco  <br/> |0  <br/> |0  <br/> |240  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

HSL(160;240;120)
  
Devuelve el índice del color azul.
  
## <a name="example-2"></a>Ejemplo 2

HSL(Hue(FillForegnd),Sat(FillForegnd),min(Lum(FillForegnd)+100,240))
  
Devuelve el índice de un color que refleja el de relleno en primer plano, aunque con mayor luminosidad.
  

