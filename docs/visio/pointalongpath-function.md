---
title: POINTALONGPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Devuelve las coordenadas de un punto en la ruta de acceso o desplazado de ésta.
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430486"
---
# <a name="pointalongpath-function"></a>Función POINTALONGPATH

Devuelve las coordenadas de un punto en la ruta de acceso o desplazado de ésta.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

POINTALONGPATH(** *section* **, ** *travel* ** *[,offset]* ** ** *[,segment]* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatorio  <br/> |**String** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
| _travel_ <br/> |Obligatorio  <br/> |**Double** <br/> |Porcentaje de la ruta de acceso atravesado, desde el punto inicial al punto final que identifica al punto. Debe oscilar entre 0 y 1.  <br/> |
| _offset_ <br/> |Opcional  <br/> |**Double** <br/> |Distancia de desplazamiento del punto respecto de la ruta de acceso. Para obtener más información, vea los comentarios.  <br/> |
| _segmentos_ <br/> |Opcional  <br/> |**Integer** <br/> |Segmento basado en 1 de la ruta de acceso en el cual se van a calcular las coordenadas.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Point**
  
## <a name="remarks"></a>Comentarios

Si  _no_ existe  _una_ sección o un segmento, Microsoft Visio devuelve #REF!. 
  
Los  *valores de*  desplazamiento positivo especifican puntos a la izquierda de la dirección de viaje. 
  
Los  *valores de*  desplazamiento negativos especifican puntos a la derecha de la dirección de viaje. 
  
Un **punto** representa un par ordenado de coordenadas geométricas (*x,y*) como valor único. 
  

