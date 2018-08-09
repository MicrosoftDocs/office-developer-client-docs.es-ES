---
title: POINTALONGPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Devuelve las coordenadas de un punto en la ruta de acceso o desplazado de ésta.
ms.openlocfilehash: 9ce6f8c171515b46aaff0ce07cbe7da4f1e958d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822775"
---
# <a name="pointalongpath-function"></a>Función POINTALONGPATH

Devuelve las coordenadas de un punto en la ruta de acceso o desplazado de ésta.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

POINTALONGPATH (** *sección* **, ** *viajes* ** ** *[, desplazamiento]* ** ** *[, segmento]* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatorio  <br/> |**String** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
| _viajes_ <br/> |Obligatorio  <br/> |**Double** <br/> |Porcentaje de la ruta de acceso atravesado, desde el punto inicial al punto final que identifica al punto. Debe oscilar entre 0 y 1.  <br/> |
| _desplazamiento_ <br/> |Opcional  <br/> |**Double** <br/> |Distancia de desplazamiento del punto respecto de la ruta de acceso. Para obtener más información, vea los comentarios.  <br/> |
| _segmento_ <br/> |Opcional  <br/> |**Integer** <br/> |Segmento basado en 1 de la ruta de acceso en el cual se van a calcular las coordenadas.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Punto**
  
## <a name="remarks"></a>Comentarios

Si no existe _section_ ni _segment_ , Microsoft Visio devuelve #REF!. 
  
Los valores de *desplazamiento* de positivo especifican puntos a la izquierda de la dirección del recorrido. 
  
Los valores de *desplazamiento* de negativos especifican puntos a la derecha de la dirección del recorrido. 
  
Un **punto** representa un par ordenado de coordenadas geométricas (*x,y*) como valor único. 
  

