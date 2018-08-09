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
ms.openlocfilehash: 50ce5a3f7caf3e716f430aa08326281c8dc847f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822845"
---
# <a name="pos-cell-character-section"></a>Celda Pos (sección Caracteres)

Determina la posición del texto de la forma con respecto a la línea base.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Posición normal  <br/> |**visPosNormal** <br/> |
| 1  <br/> | Superíndice  <br/> |**visPosSuper** <br/> |
| 2  <br/> | Subíndice  <br/> |**visPosSub** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Pos por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Char.Pos [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Pos por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionCharacter** <br/> |
| Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCharacterPos** <br/> |
   

