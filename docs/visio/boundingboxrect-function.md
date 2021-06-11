---
title: BOUNDINGBOXRECT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Devuelve la coordenada del borde especificado del cuadro de límite de la forma.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418074"
---
# <a name="boundingboxrect-function"></a>Función BOUNDINGBOXRECT

Devuelve la coordenada del borde especificado del cuadro de límite de la forma.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

BOUNDINGBOXRECT(** *Index* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Borde del cuadro de límite de la forma del cual se va a obtener la coordenada. Vea los comentarios para conocer los posibles valores.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Number**
  
## <a name="remarks"></a>Comentarios

 *Index*  puede ser uno de los siguientes valores. 
  
|**Elemento**|**Valor**|
|:-----|:-----|
|Borde izquierdo  <br/> |0  <br/> |
|Borde derecho  <br/> |1  <br/> |
|Borde superior  <br/> |2  <br/> |
|Borde inferior  <br/> |3  <br/> |
   
Si la forma tiene un elemento primario, el valor devuelto se encuentra en el sistema de coordenadas de ese elemento primario.
  

