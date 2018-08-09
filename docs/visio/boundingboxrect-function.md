---
title: BOUNDINGBOXRECT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Devuelve la coordenada del borde especificado del cuadro de límite de la forma.
ms.openlocfilehash: 2c850cb213ec0093ead53cd860f92e38da46f27e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821682"
---
# <a name="boundingboxrect-function"></a>Función BOUNDINGBOXRECT

Devuelve la coordenada del borde especificado del cuadro de límite de la forma.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

BOUNDINGBOXRECT (** *índice* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Borde del cuadro de límite de la forma del cual se va a obtener la coordenada. Vea los comentarios para conocer los posibles valores.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Número**
  
## <a name="remarks"></a>Comentarios

 *Índice* puede ser uno de los valores siguientes. 
  
|**Item**|**Valor**|
|:-----|:-----|
|Borde izquierdo  <br/> |0  <br/> |
|Borde derecho  <br/> |1  <br/> |
|Borde superior  <br/> |2  <br/> |
|Borde inferior  <br/> |3  <br/> |
   
Si la forma tiene un elemento primario, el valor devuelto está en el sistema de coordenadas de dicho elemento primario.
  

