---
title: Celda ReplaceLockShapeData (sección Cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de formas. ReplaceLockShapeData determina si los datos de formas de la forma maestra sobrescriben todos los datos de formas de la forma que se va a reemplazar.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408876"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>Celda ReplaceLockShapeData (sección Cambiar comportamiento de forma)

Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de formas. **ReplaceLockShapeData determina** si los datos de formas de la forma maestra sobrescriben todos los datos de formas de la forma que se va a reemplazar. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|1 (TRUE)  <br/> |Todas las filas y valores de la sección **Datos** de formas de la forma maestra se copian en la forma de reemplazo y se descartan los valores locales de la forma antigua que se va a reemplazar.  <br/> |
|0 (FALSE)  <br/> |Las filas y los valores de la **sección Datos de** formas de la forma maestra se copian en la forma de reemplazo. Las filas de la **sección Datos de** formas de la forma antigua con valores locales se transfieren a la forma de reemplazo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **ReplaceLockShapeData** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceLockShapeData  <br/> |
   
Para obtener una referencia desde un programa a la celda **ReplaceLockShapeData** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceLockShapeData** <br/> |
   

