---
title: Celda Pos (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: Determina la posición del texto de la forma con respecto a la línea base.
ms.openlocfilehash: d5f6823d6f55493095d29054745f62b579a47893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359818"
---
# <a name="pos-cell-character-section"></a>Celda Pos (Sección de caracteres)

Determina la posición del texto de la forma con respecto a la línea base.
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Posición normal  <br/> |**visPosNormal** <br/> |
| 1  <br/> | Superscript  <br/> |**visPosSuper** <br/> |
| segundo  <br/> | Subscript  <br/> |**visPosSub** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Pos por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Char. pos [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Pos por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionCharacter** <br/> |
| Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCharacterPos** <br/> |
   

