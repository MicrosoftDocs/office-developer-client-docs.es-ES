---
title: Celda ReplaceCopyCells (Sección de comportamiento de cambio de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Indica una lista de celdas de ShapeSheet que se copian de una forma antigua a la forma de reemplazo durante una operación de reemplazo de forma.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409345"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>Celda ReplaceCopyCells (Sección de comportamiento de cambio de forma)

Indica una lista de celdas de ShapeSheet que se copian de una forma antigua a la forma de reemplazo durante una operación de reemplazo de forma. 
  
## <a name="remarks"></a>Comentarios

La forma maestra del reemplazo debe contener una llamada de función **DEPENDSON** en la celda **ReplaceCopyCells,** donde cada argumento de la función es una referencia a una celda. Dichas celdas se copian de la forma antigua a la forma resultante de una operación de reemplazo de forma, independientemente de dónde se encuentran en shapeSheet. 
  
Los valores o fórmulas que hacen referencia a otras celdas se copian en la forma resultante. Si la forma resultante no tiene la celda a la que se hace referencia, la celda copiada sólo contiene el valor. 
  
Las referencias de la celda **ReplaceCopyCells** invalidan  la protección establecida en las celdas según se define en la sección Protección y las celdas **ReplaceLockFormat**, **ReplaceLockShapeData** y **ReplaceLockText.** 
  
Para obtener una referencia a la celda **ReplaceCopyCells** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceCopyCells  <br/> |
   
Para obtener una referencia desde un programa a la celda **ReplaceCopyCells** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceCopyCells** <br/> |
   

