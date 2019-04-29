---
title: Celda ReplaceCopyCells (sección cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indica una lista de las celdas de ShapeSheet que se copian de una forma antigua a la nueva forma durante una operación de reemplazo de formas.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409345"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>Celda ReplaceCopyCells (sección cambiar comportamiento de forma)

Indica una lista de las celdas de ShapeSheet que se copian de una forma antigua a la nueva forma durante una operación de reemplazo de formas. 
  
## <a name="remarks"></a>Comentarios

La forma de patrón de la sustitución debe contener una llamada a la función **DEPENDSON** en la celda **ReplaceCopyCells** , donde cada argumento de la función es una referencia a una celda. Esas celdas se copian de la forma antigua a la forma que resulta de una operación de reemplazo de forma, independientemente de dónde se encuentren en la ShapeSheet. 
  
Los valores y las fórmulas que hacen referencia a otras celdas se copian en la forma resultante. Si la forma resultante no tiene la celda a la que se hace referencia, la celda copiada sólo contendrá el valor. 
  
Las referencias en la celda **ReplaceCopyCells** se configuran protección en las celdas como se define en la sección **protección** y en las celdas **ReplaceLockFormat**, **ReplaceLockShapeData**y **ReplaceLockText** . 
  
Para obtener una referencia a la celda **ReplaceCopyCells** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceCopyCells  <br/> |
   
Para obtener una referencia desde un programa a la celda **ReplaceCopyCells** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceCopyCells** <br/> |
   

