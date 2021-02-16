---
title: Celda DirY / B (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Determina el componente y para el vector de alineación necesario de un punto de conexión correspondiente. También se utiliza para orientar el segmento adjunto de un conector dinámico. Esta celda acepta valores de punto flotante.
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417094"
---
# <a name="diry--b-cell-connection-points-section"></a>Celda DirY / B (Sección de puntos de conexión)

Determina el componente  *y para*  el vector de alineación necesario de un punto de conexión correspondiente. También se utiliza para orientar el segmento adjunto de un conector dinámico. Esta celda toma valores de punto flotante. 
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda DirY / B por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Connections.DirY[ *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda DirY / B por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionConnectionPts** <br/> |
|Índice de fila:  <br/> |**visRowConnectionPts**  +   *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCnnctDirY** (filas no extendidas)           **visCnnctB** (filas extendidas)  <br/> |
   
Para obtener información sobre las filas extensibles y no extensibles, vea la fila de puntos de conexión.
  

