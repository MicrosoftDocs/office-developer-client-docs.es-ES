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
ms.openlocfilehash: 804faeb24932e414ad03bc9e8487c62ca08bd7d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341478"
---
# <a name="angletoloc-function"></a>Función ANGLETOLOC

Devuelve un ángulo transformado en el sistema de coordenadas local de la forma de destino. Convierte las coordenadas locales de un ángulo en una forma de origen a las coordenadas locales en una forma de destino. 
  
## <a name="syntax"></a>Sintaxis

ANGLETOLOC (* * *srcAngle* * *, * * *srcRef* * *, * * *dstRef* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Un ángulo en el sistema de coordenadas de origen.  <br/> |
| _srcRef_ <br/> |Obligatorio  <br/> |**String** <br/> | Una referencia a una celda en el objeto de origen, como una forma, grupo, página, etcétera.  <br/> |
| _dstRef_ <br/> |Obligatorio  <br/> |**String** <br/> |Una referencia a una celda en el objeto de destino, como una forma, grupo, página, etcétera.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede usar la función ÁNGULOALOC para establecer celdas de ángulo local en una forma en términos de un ángulo desde otro espacio de coordenadas.
  
Esta función sirve incluso en el caso de que las formas de origen y de destino formen parte de grupos. También ajusta el giro y el volteo en la transformación intermedia.
  
Las coordenadas de origen y de destino deben encontrarse en la misma página.
  

