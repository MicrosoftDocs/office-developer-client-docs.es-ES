---
title: Celda LockMoveX (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Bloquea la posición horizontal de la forma de manera que ésta no se puede desplazar horizontalmente.
ms.openlocfilehash: af0cee32370a540cd8d7aaf960cc0cbc27cc8f97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435862"
---
# <a name="lockmovex-cell-protection-section"></a>Celda LockMoveX (Sección de protección)

Bloquea la posición horizontal de la forma de manera que ésta no se puede desplazar horizontalmente.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La posición horizontal se encuentra bloqueada.  <br/> |
| FALSE  <br/> | La posición horizontal no se encuentra bloqueada.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockMoveX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockMoveX  <br/> |
   
Para obtener una referencia desde un programa a la celda LockMoveX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockMoveX** <br/> |
   

