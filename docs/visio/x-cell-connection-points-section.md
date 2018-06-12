---
title: Celda X (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Representa la x-coordenadas de un punto de conexión en coordenadas locales.
ms.openlocfilehash: 27821f9aa94f97d8e019d7c7307c036549bf807b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823559"
---
# <a name="x-cell-connection-points-section"></a>Celda X (Sección de puntos de conexión)

Representa la *x* -coordenadas de un punto de conexión en coordenadas locales. 
  
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Propiedad *i* donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda X por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionConnectionPts** <br/> |
| Índice de fila:  <br/> |**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visX** <br/> |
   

