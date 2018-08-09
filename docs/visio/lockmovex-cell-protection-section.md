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
ms.openlocfilehash: 981f4f417e48f70d0693e30683c4351d0e53a758
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822531"
---
# <a name="lockmovex-cell-protection-section"></a>Celda LockMoveX (sección Protección)

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
   

