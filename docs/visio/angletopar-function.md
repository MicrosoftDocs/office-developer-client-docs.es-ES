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
ms.openlocfilehash: 3a739c55d568dc548f8175b56f22e6ec4c28e4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821539"
---
# <a name="angletopar-function"></a>Función ANGLETOPAR

Devuelve un ángulo transformado en el sistema de coordenadas principales de la forma de destino. Convierte las coordenadas locales de un ángulo en una forma de origen a las coordenadas originales en una forma de destino.
    
 
  
## <a name="syntax"></a>Sintaxis

ANGLETOPAR (** *ánguloOrigen* **, ** *refOrigen* **, ** *refDestino* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _ánguloOrigen_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Un ángulo en el sistema de coordenadas de origen.  <br/> |
| _refOrigen_ <br/> |Obligatorio  <br/> |**String** <br/> | Una referencia a una celda en el objeto de origen, como una forma, grupo, página, etcétera.  <br/> |
| _refDestino_ <br/> |Obligatorio  <br/> |**String** <br/> |Una referencia a una celda en el objeto de destino, como una forma, grupo, página, etcétera.  <br/> |
   
## <a name="remarks"></a>Observaciones

Esta función sirve incluso en el caso de que las formas de origen y de destino formen parte de grupos. También ajusta el giro y el volteo en la transformación intermedia.
  
Las coordenadas de origen y de destino deben encontrarse en la misma página.
  
Si el destino es una página que carece de forma principal, el resultado se expresará en las coordenadas locales de la página.
  

