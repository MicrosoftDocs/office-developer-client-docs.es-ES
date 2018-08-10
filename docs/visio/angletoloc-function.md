---
title: ANGLETOLOC (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
localization_priority: Normal
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: Devuelve un ángulo transformado en el sistema de coordenadas local de la forma de destino. Convierte las coordenadas locales de un ángulo en una forma de origen a las coordenadas locales en una forma de destino.
ms.openlocfilehash: 09ab0a4a55446dd74729f1da0bcf022d8376909b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821531"
---
# <a name="angletoloc-function"></a>Función ANGLETOLOC

Devuelve un ángulo transformado en el sistema de coordenadas local de la forma de destino. Convierte las coordenadas locales de un ángulo en una forma de origen a las coordenadas locales en una forma de destino. 
    
 
  
## <a name="syntax"></a>Sintaxis

ANGLETOLOC (** *ánguloOrigen* **, ** *refOrigen* **, ** *refDestino* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _ánguloOrigen_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Un ángulo en el sistema de coordenadas de origen.  <br/> |
| _refOrigen_ <br/> |Obligatorio  <br/> |**String** <br/> | Una referencia a una celda en el objeto de origen, como una forma, grupo, página, etcétera.  <br/> |
| _refDestino_ <br/> |Obligatorio  <br/> |**String** <br/> |Una referencia a una celda en el objeto de destino, como una forma, grupo, página, etcétera.  <br/> |
   
## <a name="remarks"></a>Observaciones

Puede usar la función ÁNGULOALOC para establecer celdas de ángulo local en una forma en términos de un ángulo desde otro espacio de coordenadas.
  
Esta función sirve incluso en el caso de que las formas de origen y de destino formen parte de grupos. También ajusta el giro y el volteo en la transformación intermedia.
  
Las coordenadas de origen y de destino deben encontrarse en la misma página.
  

