---
title: Celda Font (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Representa el número de la fuente empleada para dar formato al texto. Los números de fuente varían de acuerdo con las fuentes que tenga instaladas en el sistema. El número 0 representa la fuente predeterminada, que suele ser Arial.
ms.openlocfilehash: d9182932b8fa63c30473b93e420aa9efe30bf5eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438669"
---
# <a name="font-cell-character-section"></a>Celda Font (Sección de caracteres)

Representa el número de la fuente empleada para dar formato al texto. Los números de fuente varían de acuerdo con las fuentes que tenga instaladas en el sistema. El número 0 representa la fuente predeterminada, que suele ser Arial.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Font por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Char. Font [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Font por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionCharacter** <br/> |
| Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCharacterFont** <br/> |
   

