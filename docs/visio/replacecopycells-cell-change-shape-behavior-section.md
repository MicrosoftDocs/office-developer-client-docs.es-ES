---
title: Celda ReplaceCopyCells (sección Cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indica una lista de las celdas de ShapeSheet que se copian desde una forma antigua a la forma de reemplazo durante una operación de reemplazo de la forma.
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822943"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>Celda ReplaceCopyCells (sección Cambiar comportamiento de forma)

Indica una lista de las celdas de ShapeSheet que se copian desde una forma antigua a la forma de reemplazo durante una operación de reemplazo de la forma. 
  
## <a name="remarks"></a>Comentarios

La forma de patrón de la sustitución debe contener una llamada de función **DEPENDSON** en la celda **ReplaceCopyCells** , donde cada argumento de la función es una referencia a una celda. Esas celdas se copian de la antigua forma a la forma que dan como resultado de una operación de reemplazo de la forma, independientemente de dónde se encuentran en la ShapeSheet. 
  
Los valores y las fórmulas que hacen referencia otras celdas se copian a la forma resultante. Si la forma resultante no tiene la celda que se hace referencia, la celda copiada contiene sólo el valor. 
  
Referencias de la celda **ReplaceCopyCells** reemplazar el conjunto de protección en las celdas como se define en la sección de **protección** y la **ReplaceLockFormat**, **ReplaceLockShapeData**y **ReplaceLockText** celdas. 
  
Para obtener una referencia a la celda **ReplaceCopyCells** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceCopyCells  <br/> |
   
Para obtener una referencia a la celda **ReplaceCopyCells** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceCopyCells** <br/> |
   

