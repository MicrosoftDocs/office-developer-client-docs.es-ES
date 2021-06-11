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
description: Contiene las coordenadas x - e y del punto central de la elipse y dos puntos en la elipse.
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421833"
---
# <a name="ellipse-row-geometry-section"></a>Fila Ellipse (Sección de Geometría)

Contiene las  *coordenadas x*  -  *e y*  del punto central de la elipse y dos puntos en la elipse. 
  
Las filas Ellipse contienen las celdas siguientes.
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordenada  *x*  del punto central.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordenada  *y*  del punto central.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordenada x de un punto en la elipse; emparejado con  *y*  -coordinate representado por la celda B.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |La coordenada  *y*  de un punto en la elipse; emparejado con una coordenada x representada por la celda A.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |La coordenada  *x*  de otro punto de la elipse; emparejado con  *y*  -coordinate representado por la celda D.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |La coordenada  *y*  de otro punto de la elipse; emparejado con  *y*  -coordinate representado por la celda C.  <br/> |
   
## <a name="remarks"></a>Comentarios

Una sección de geometría que contenga una fila Ellipse o InfiniteLine no debe contener otras filas.
  

