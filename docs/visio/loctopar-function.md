---
title: LOCTOPAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: Devuelve un punto transformado en las coordenadas primarias del sistema de coordenadas de destino.
ms.openlocfilehash: 65a08837d7d026836ebc8d5e35938ea049d005e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439985"
---
# <a name="loctopar-function"></a>Función LOCTOPAR

Devuelve un punto transformado en las coordenadas primarias del sistema de coordenadas de destino.
  
## <a name="syntax"></a>Sintaxis

LOCTOPAR(** *srcPoint* **, ** *srcRef* **, ** *dstRef* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _srcPoint_ <br/> |Obligatorio  <br/> |**String** <br/> | Punto del sistema de coordenadas de origen, en las coordenadas locales.  <br/> |
| _srcRef_ <br/> |Obligatorio  <br/> |**String** <br/> | Referencia a una celda en el objeto de origen.  <br/> |
| _dstRef_ <br/> |Obligatorio  <br/> |**String** <br/> | Referencia a una celda en el objeto de destino.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Comentarios

Convierte las coordenadas locales de un punto en una forma de origen a las coordenadas principales en una forma de destino. Puede utilizar la función LOCTOPAR para establecer coordenadas principales en las celdas, como PinX, PinY, BeginX y BeginY en una forma utilizando otro punto de un sistema de coordenadas distinto. 
  
Esta función sirve incluso en el caso de que las formas de origen y de destino formen parte de grupos. También ajusta el giro y el volteo en la transformación intermedia. 
  
Las coordenadas de origen y de destino deben encontrarse en la misma página. 
  
Si el destino es una página que carece de forma principal, el resultado se expresará en las coordenadas locales de la página. 
  
## <a name="example"></a>Ejemplo

LOCTOPAR(PNT(LocPinX, LocPinY), Width, Hoja.4!Width) 
  
Convierte el eje local de la forma asociada con la fórmula a las coordenadas principales de la Hoja.4. 
  

