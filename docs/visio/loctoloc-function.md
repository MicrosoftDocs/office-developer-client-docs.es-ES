---
title: LOCTOLOC (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
localization_priority: Normal
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: Devuelve un punto transformado en coordenadas locales en el sistema de coordenadas de destino.
ms.openlocfilehash: f08feb6137c3022027d19b45f06285fb8b6441a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358040"
---
# <a name="loctoloc-function"></a>Función LOCTOLOC

Devuelve un punto transformado en coordenadas locales en el sistema de coordenadas de destino.
  
## <a name="syntax"></a>Sintaxis

LOCTOLOC (* * *srcPoint* * *, * * *srcRef* * *, * * *dstRef* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _srcPoint_ <br/> |Obligatorio  <br/> |**String** <br/> | Punto del sistema de coordenadas de origen, en las coordenadas locales.  <br/> |
| _srcRef_ <br/> |Obligatorio  <br/> |**String** <br/> | Referencia a una celda en el objeto de origen.  <br/> |
| _dstRef_ <br/> |Obligatorio  <br/> |**String** <br/> | Referencia a una celda en el objeto de destino.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

La función LOCTOLOC convierte las coordenadas locales de un punto en una forma de origen a las coordenadas locales en una forma de destino. Puede utilizar esta función para construir una forma, por ejemplo, usando como referencia un punto de otro espacio de coordenadas distinto. También puede utilizar esta función para convertir un punto local en sus coordenadas de página o viceversa.
  
Esta función sirve incluso en el caso de que las formas de origen y de destino formen parte de grupos. También ajusta el giro y el volteo en la transformación intermedia.
  
Las coordenadas de origen y de destino deben encontrarse en la misma página.
  
## <a name="example"></a>Ejemplo

La siguiente fórmula convierte el eje local de la forma asociada con la fórmula en un punto de la página.
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


