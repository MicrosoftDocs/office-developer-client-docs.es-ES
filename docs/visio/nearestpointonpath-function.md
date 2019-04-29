---
title: NEARESTPOINTONPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Devuelve el porcentaje (como un valor entre 0 y 1) de la distancia a lo largo de la ruta de acceso del punto que se encuentra más cerca de las coordenadas especificadas.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407336"
---
# <a name="nearestpointonpath-function"></a>Función NEARESTPOINTONPATH

Devuelve el porcentaje (como un valor entre 0 y 1) de la distancia a lo largo de la ruta de acceso del punto que se encuentra más cerca de las coordenadas especificadas.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

NEARESTPOINTONPATH (* * *sección* * *, * * *x* * *, * * *y* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatorio  <br/> |**String** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
| _x_ <br/> |Obligatorio  <br/> |**Double** <br/> |Coordenada _x_del punto especificado.  <br/> |
| _y_ <br/> |Obligatorio  <br/> |**Double** <br/> |Coordenada _y_del punto especificado.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Double**
  
## <a name="remarks"></a>Comentarios

Si _section_ no existe, Microsoft Visio devuelve #REF!. 
  

