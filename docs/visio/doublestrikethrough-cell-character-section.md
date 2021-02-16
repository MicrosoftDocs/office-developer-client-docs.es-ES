---
title: Celda DoubleStrikethrough (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: Determina si el texto tiene formato de doble tachado.
ms.openlocfilehash: d8ef5bdb6e086be9657f51c66c10d578414e1deb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360595"
---
# <a name="doublestrikethrough-cell-character-section"></a>Celda DoubleStrikethrough (Sección de caracteres)

Determina si el texto tiene formato de doble tachado.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda DoubleStrikethrough por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Char.DoubleStrikethrough[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda DoubleStrikethrough por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionCharacter** <br/> |
| Índice de fila:  <br/> |**visRowCharacter**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCharacterDoubleStrikethrough** <br/> |
   

