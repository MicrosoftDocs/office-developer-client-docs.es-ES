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
ms.openlocfilehash: 6666d47555f8175b4950f95e1fb15abb8b11bfd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348352"
---
# <a name="lockmovey-cell-protection-section"></a>Celda LockMoveY (Sección de protección)

Bloquea la posición vertical de la forma de manera que ésta no se pueda desplazar verticalmente.
  
|**Value**|**Descripción**|
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
   

