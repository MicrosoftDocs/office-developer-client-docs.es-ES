---
title: Celda Overline (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Determina si el texto tiene una línea encima.
ms.openlocfilehash: d5df39c2f12890d5fb4881346516abdb4f2b8099
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431648"
---
# <a name="overline-cell-character-section"></a>Celda Overline (Sección de caracteres)

Determina si el texto tiene una línea encima.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El texto tiene una línea encima.  <br/> |
|FALSE  <br/> |El texto no tiene una línea encima.  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede usar el cuadro de diálogo **Texto** para establecer el valor de esta celda (en la ficha **Inicio**, haga clic en la flecha de **Fuente**). 
  
Para obtener una referencia a la celda Overline por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char. Overline [ *i* ] donde *i* = <1>, 2. 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Overline por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterOverline** <br/> |
   

