---
title: Celda LockCalcWH (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Bloquea un rectángulo de selección de una forma de modo que no se pueda volver a calcular cuando se modifique un vértice o se cambie un tipo de fila en la sección de geometría.
ms.openlocfilehash: 2b1d907f480a22a56f5847035da8d1cbde5fdcc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423044"
---
# <a name="lockcalcwh-cell-protection-section"></a>Celda LockCalcWH (Sección de protección)

Bloquea un rectángulo de selección de una forma de modo que no se pueda volver a calcular cuando se modifique un vértice o se cambie un tipo de fila en la sección de geometría.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El ancho y el alto no pueden volver a calcularse.  <br/> |
| FALSE  <br/> | El ancho y el alto pueden volver a calcularse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockCalcWH por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockCalcWH  <br/> |
   
Para obtener una referencia desde un programa a la celda LockCalcWH por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockCalcWH** <br/> |
   

