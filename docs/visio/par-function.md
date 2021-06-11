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
description: Devuelve las coordenadas x,y de un punto en el sistema de coordenadas del elemento primario de la forma.
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414511"
---
# <a name="par-function"></a>Función PAR

Devuelve las  _coordenadas x,y_ de un punto en el sistema de coordenadas del elemento primario de la forma. 
  
## <a name="syntax"></a>Sintaxis

PAR(** *point* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _punto_ <br/> |Obligatorio  <br/> |**Number, Number** <br/> |Coordenadas del punto en el sistema de coordenadas de la forma actual.  <br/> |
   
## <a name="remarks"></a>Comentarios

En Microsoft Visio, un punto es un valor único que incluye un par de *coordenadas x* e *y.* Si la forma se encuentra en un grupo, su forma principal es el propio grupo. Si no se encuentra en un grupo, su forma principal es la página. 
  
## <a name="example"></a>Ejemplo

PAR(PNT(PinX,PinY)) 
  
En esta expresión, PNT convierte en un punto un par de coordenadas dentro de la forma actual. PAR convierte a continuación el punto en un par de coordenadas cuyo origen es la esquina inferior izquierda de la página o del grupo que contiene la forma actual. 
  

