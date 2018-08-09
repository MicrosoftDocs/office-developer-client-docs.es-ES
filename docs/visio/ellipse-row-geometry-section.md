---
title: Fila Ellipse (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Contiene x - e y-las coordenadas del punto central y dos puntos de la elipse de la elipse.
ms.openlocfilehash: 0a2acb0efa20f67d04581f827edbfc4fb4a2d6b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822054"
---
# <a name="ellipse-row-geometry-section"></a>Fila Ellipse (sección Geometría)

Contiene el *x* - e *y* -las coordenadas del punto central y dos puntos de la elipse de la elipse. 
  
Las filas Ellipse contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La *x* -coordenadas del punto central.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La *y* -coordenadas del punto central.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |La coordenada x de un punto de la elipse; emparejada con la *y* -coordenada representada por la celda B.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |La *y* -coordenadas de un punto de la elipse; emparejada con la coordenada x representada por la celda A.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |La *x* -coordenadas de otro punto de la elipse; emparejada con la *y* -coordenada representada por la celda D.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |La *y* -coordenadas de otro punto de la elipse; emparejada con la *y* -representada por la celda C de coordenadas.  <br/> |
   
## <a name="remarks"></a>Comentarios

Una sección de geometría que contenga una fila Ellipse o InfiniteLine no debe contener otras filas.
  

