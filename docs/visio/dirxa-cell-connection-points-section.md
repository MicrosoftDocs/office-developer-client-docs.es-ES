---
title: Celda DirX / A (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Determina el componente x para el vector de alineación necesario de un punto de conexión coincidentes. También se utiliza para orientar el segmento adjunto de un conector dinámico. Esta celda toma valores de punto flotante.
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422400"
---
# <a name="dirx--a-cell-connection-points-section"></a>Celda DirX / A (sección de puntos de conexión)

Determina el componente *x* para el vector de alineación necesario de un punto de conexión coincidentes. También se utiliza para orientar el segmento adjunto de un conector dinámico. Esta celda toma valores de punto flotante. 
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda DirX / A por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Connections. DirX [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda DirX / A por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionConnectionPts** <br/> |
| Índice de fila:  <br/> |**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2  <br/> |
| Índice de celda:  <br/> |**visCnnctDirX** (filas no extensibles)           **visCnnctA** (filas extendidas)  <br/> |
   
Para obtener información sobre las filas extensibles y no extensibles, vea la fila de puntos de conexión.
  

