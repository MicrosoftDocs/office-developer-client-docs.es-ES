---
title: Celda Strikethru (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Determina si el texto tiene el formato tachado.
ms.openlocfilehash: 2b25d1d9b00d062214c02c3fc7b14569b43a5110
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823339"
---
# <a name="strikethru-cell-character-section"></a>Celda Strikethru (sección Caracteres)

Determina si el texto tiene el formato tachado.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El texto tiene el formato tachado.  <br/> |
|FALSE  <br/> |El texto no tiene el formato tachado.  <br/> |
   
## <a name="remarks"></a>Observaciones

También puede usar el cuadro de diálogo **Texto** para establecer el valor de esta celda (en la ficha **Inicio**, haga clic en la flecha de **Fuente**). 
  
Para obtener una referencia a la celda Strikethru por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char.Strikethru [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Strikethru por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterStrikethru** <br/> |
   

