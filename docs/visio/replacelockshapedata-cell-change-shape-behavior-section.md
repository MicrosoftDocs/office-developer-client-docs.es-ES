---
title: Celda ReplaceLockShapeData (sección cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma. ReplaceLockShapeData determina si los datos de formas de la forma de patrón sobrescribirán todos los datos de formas de la forma que se va a reemplazar.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408876"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>Celda ReplaceLockShapeData (sección cambiar comportamiento de forma)

Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma. **ReplaceLockShapeData** determina si los datos de formas de la forma de patrón sobrescribirán todos los datos de formas de la forma que se va a reemplazar. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|1 (TRUE)  <br/> |Todas las filas y valores de la sección **datos de formas** de la forma de patrón se copian en la forma de reemplazo y se descartan todos los valores locales de la forma antigua que se va a reemplazar.  <br/> |
|0 (FALSO)  <br/> |Las filas y los valores de la sección **datos de formas** de la forma de patrón se copian a la nueva forma. Las filas de la sección **datos de formas** de la forma antigua con valores locales se transfieren a la nueva forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **ReplaceLockShapeData** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceLockShapeData  <br/> |
   
Para obtener una referencia desde un programa a la celda **ReplaceLockShapeData** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceLockShapeData** <br/> |
   

