---
title: Celda Position (Sección de tabulaciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Especifica la posición de una tabulación. La posición de tabulación no depende de la escala del dibujo. Si se cambia la escala, la posición de tabulación permanece igual.
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307752"
---
# <a name="position-cell-tabs-section"></a>Celda Position (Sección de tabulaciones)

Especifica la posición de una tabulación. La posición de tabulación no depende de la escala del dibujo. Si se cambia la escala, la posición de tabulación permanece igual.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Position por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Etiquetas.  *ij* donde *i* y *j* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Position por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionTab** <br/> |
| Índice de fila:  <br/> |**visRowTab** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> | (*j* * 3) + **visTabPos** <br/> |
   

