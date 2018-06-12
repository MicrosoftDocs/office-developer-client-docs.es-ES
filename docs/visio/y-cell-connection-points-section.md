---
title: Celda Y (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Representa la y-coordenadas de un punto de conexión en coordenadas locales.
ms.openlocfilehash: 270ae98789e29ca170f260aa70e951d4b2af2962
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823573"
---
# <a name="y-cell-connection-points-section"></a>Celda Y (Sección de puntos de conexión)

Representa la *y* -coordenadas de un punto de conexión en coordenadas locales. 
  
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda Y por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Connections.Y *i* donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Y por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionConnectionPts** <br/> |
| Índice de fila:  <br/> |**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visY** <br/> |
   

