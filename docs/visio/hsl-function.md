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
description: Devuelve un valor que representa un índice en la paleta de colores del documento. Especifica un color por sus componentes de matiz, saturación y luminosidad.
ms.openlocfilehash: 55703239395c54beedf4b7383435253f9c37006f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420965"
---
# <a name="hsl-function"></a>Función HSL

Devuelve un valor que representa un índice en la paleta de colores del documento. Especifica un color por sus componentes de matiz, saturación y luminosidad.
  
## <a name="syntax"></a>Sintaxis

HSL (* * *matiz* * *, * * *saturación* * *, * * *luminosidad* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _matiz_ <br/> |Obligatorio  <br/> |**Number** <br/> |El matiz del color, expresado como un número comprendido entre 0 y 239, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.  <br/> |
| _saturación_ <br/> |Obligatorio  <br/> |**Number** <br/> |La saturación del color, expresada como un número comprendido entre 0 y 240, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.  <br/> |
| _luminosidad_ <br/> |Obligatorio  <br/> |**Number** <br/> | La luminosidad del color, expresada como un número comprendido entre 0 y 240, ambos incluidos, o una expresión que da como resultado un número de ese intervalo.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

Si el color que devuelve la función no forma parte de la paleta de colores del documento actual, se agregará a la lista de colores disponibles del documento. 
  
La tabla siguiente muestra varios colores estándar y los valores correspondientes al matiz, saturación y luminosidad. 
  
|**Color**|**Valor de matiz**|**Valor de saturación**|**Valor de luminosidad**|
|:-----|:-----|:-----|:-----|
|Negro  <br/> |comprendi  <br/> |comprendi  <br/> |apartado  <br/> |
|Azul  <br/> |160  <br/> |240  <br/> |120  <br/> |
|Verde  <br/> |80  <br/> |240  <br/> |120  <br/> |
|Aguamarina  <br/> |120  <br/> |240  <br/> |120  <br/> |
|Rojo  <br/> |comprendi  <br/> |240  <br/> |120  <br/> |
|Magenta  <br/> |200  <br/> |240  <br/> |120  <br/> |
|Amarillo  <br/> |40  <br/> |240  <br/> |120  <br/> |
|Blanco  <br/> |comprendi  <br/> |comprendi  <br/> |240  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

HSL (160240120)
  
Devuelve el índice del color azul.
  
## <a name="example-2"></a>Ejemplo 2

HSL (matiz (FillForegnd), SAT (FillForegnd), MIN (LUM (FillForegnd) + 100240))
  
Devuelve el índice de un color que refleja el de relleno en primer plano, aunque con mayor luminosidad.
  

