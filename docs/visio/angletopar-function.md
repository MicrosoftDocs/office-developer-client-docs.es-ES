---
title: ANGLETOPAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
localization_priority: Normal
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: Devuelve un ángulo transformado en el sistema de coordenadas principales de la forma de destino. Convierte las coordenadas locales de un ángulo en una forma de origen a las coordenadas originales en una forma de destino.
ms.openlocfilehash: 0fed51e264bfb21da25d4e91f20f4bc0803e46e8
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160261"
---
# <a name="angletopar-function"></a>Función ANGLETOPAR

Devuelve un ángulo transformado en el sistema de coordenadas principales de la forma de destino. Convierte las coordenadas locales de un ángulo en una forma de origen a las coordenadas originales en una forma de destino.
    
 
  
## <a name="syntax"></a>Sintaxis

ANGLETOPAR(***srcAngle***, ***srcRef***, ***dstRef*** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Un ángulo en el sistema de coordenadas de origen.  <br/> |
| _srcRef_ <br/> |Obligatorio  <br/> |**String** <br/> | Una referencia a una celda en el objeto de origen, como una forma, grupo, página, etcétera.  <br/> |
| _dstRef_ <br/> |Obligatorio  <br/> |**String** <br/> |Una referencia a una celda en el objeto de destino, como una forma, grupo, página, etcétera.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta función sirve incluso en el caso de que las formas de origen y de destino formen parte de grupos. También ajusta el giro y el volteo en la transformación intermedia.
  
Las coordenadas de origen y de destino deben encontrarse en la misma página.
  
Si el destino es una página que carece de forma principal, el resultado se expresará en las coordenadas locales de la página.
  

