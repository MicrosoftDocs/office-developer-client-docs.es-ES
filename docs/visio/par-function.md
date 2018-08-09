---
title: PAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Devuelve las coordenadas x, y de un punto en el sistema de coordenadas de principal la forma.
ms.openlocfilehash: a3f7afd3f9bc988a20526451a6d7d7081d27a2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822729"
---
# <a name="par-function"></a>Función PAR

Devuelve las coordenadas _x, y_ de un punto en el sistema de coordenadas de principal la forma. 
  
## <a name="syntax"></a>Sintaxis

NOMINAL (** *Elija* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _punto_ <br/> |Obligatorio  <br/> |**Number, Number** <br/> |Coordenadas del punto en el sistema de coordenadas de la forma actual.  <br/> |
   
## <a name="remarks"></a>Comentarios

En Microsoft Visio, un punto es un valor único que incluye un par de *x* e *y* -coordenadas. Si la forma está en un grupo, su elemento primario es el grupo. Si la forma no es un grupo, su forma principal es la página. 
  
## <a name="example"></a>Ejemplo

PAR(PNT(PinX,PinY)) 
  
En esta expresión, PNT convierte en un punto un par de coordenadas dentro de la forma actual. PAR convierte a continuación el punto en un par de coordenadas cuyo origen es la esquina inferior izquierda de la página o del grupo que contiene la forma actual. 
  

