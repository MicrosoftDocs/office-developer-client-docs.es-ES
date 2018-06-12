---
title: Celda LockHeight (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Bloquea el ancho de la forma de manera que éste permanece inalterado al ajustar el tamaño de la forma.
ms.openlocfilehash: f6afe6037ff3d0810cc532bbc18bb749ee589bb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822514"
---
# <a name="lockheight-cell-protection-section"></a>Celda LockHeight (Sección de protección)

Bloquea el ancho de la forma de manera que éste permanece inalterado al ajustar el tamaño de la forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El alto se encuentra bloqueado.  <br/> |
| FALSE  <br/> | El alto no se encuentra bloqueado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockHeight  <br/> |
   
Para obtener una referencia a la celda LockHeight por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockHeight** <br/> |
   

