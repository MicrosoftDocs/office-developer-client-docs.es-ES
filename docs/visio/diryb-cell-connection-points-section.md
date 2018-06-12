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
description: Determina la y-component para el vector de alineación necesario de un punto de conexión coincidente. También se usa para orientar el segmento adjunto de un conector dinámico. Esta celda acepta flotante valor de punto.
ms.openlocfilehash: e650e598b1e47d666b2700d683a17300d3a8e67d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821971"
---
# <a name="diry--b-cell-connection-points-section"></a>Celda DirY / B (Sección de puntos de conexión)

Determina la *y* -component para el vector de alineación necesario de un punto de conexión coincidente. También se usa para orientar el segmento adjunto de un conector dinámico. Esta celda acepta flotante valor de punto. 
  
## <a name="remarks"></a>Notas

Para obtener una referencia a la DirY / B celda por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Connections.DirY [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la DirY / B celda por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionConnectionPts** <br/> |
|Índice de fila:  <br/> |**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCnnctDirY** (filas no extensibles)           **visCnnctB** (filas extensibles)  <br/> |
   
Para obtener información sobre las filas extensibles y no extensibles, vea la fila de puntos de conexión.
  

