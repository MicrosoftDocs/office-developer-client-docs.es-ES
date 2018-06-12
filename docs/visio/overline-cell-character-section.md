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
ms.openlocfilehash: 3ceb0f5bcb6f66098938e49ea5f176921d0c9808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822700"
---
# <a name="overline-cell-character-section"></a>Celda Overline (Sección de caracteres)

Determina si el texto tiene una línea encima.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El texto tiene una línea encima.  <br/> |
|FALSE  <br/> |El texto no tiene una línea encima.  <br/> |
   
## <a name="remarks"></a>Observaciones

También puede establecer el valor de esta celda mediante el cuadro de diálogo **texto** (en la ficha **Inicio** , haga clic en la flecha de **fuente** ). 
  
Para obtener una referencia a la celda Overline por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char.Overline [ *i* ] donde *i* = < 1 >, 2. 3 …  <br/> |
   
Para obtener una referencia a la celda Overline por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterOverline** <br/> |
   

