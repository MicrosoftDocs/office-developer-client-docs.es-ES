---
title: Celda LockMoveY (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Bloquea la posición vertical de la forma de manera que ésta no se pueda desplazar verticalmente.
ms.openlocfilehash: 24f6f477860ea3634cfdcfd92199f2de65e543db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822513"
---
# <a name="lockmovey-cell-protection-section"></a>Celda LockMoveY (sección Protección)

Bloquea la posición vertical de la forma de manera que ésta no se pueda desplazar verticalmente.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La posición vertical se encuentra bloqueada.  <br/> |
| FALSE  <br/> | La posición vertical no se encuentra bloqueada.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockMoveY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockMoveY  <br/> |
   
Para obtener una referencia desde un programa a la celda LockMoveY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockMoveY** <br/> |
   

