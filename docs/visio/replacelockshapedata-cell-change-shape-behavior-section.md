---
title: Celda ReplaceLockShapeData (sección Cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma. El ReplaceLockShapeData determina si los datos de formas de la forma de patrón sobrescriben todos los datos de la forma de la forma reemplazada.
ms.openlocfilehash: 07547140c7c96e49663270e51a90fd559afedf29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822978"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>Celda ReplaceLockShapeData (sección Cambiar comportamiento de forma)

Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma. El **ReplaceLockShapeData** determina si los datos de formas de la forma de patrón sobrescriben todos los datos de la forma de la forma reemplazada. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|1 (TRUE)  <br/> |Todas las filas y valores de la sección **Datos de formas** de la forma de patrón se copian en la forma de reemplazo y los valores locales de la forma antigua reemplazada se descartan.  <br/> |
|0 (FALSO)  <br/> |Las filas y valores de la sección **Datos de formas** de la forma de patrón se copian en la nueva forma. Todas las filas en la sección **Datos de formas** de la forma antigua con valores locales se transfieren a la nueva forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **ReplaceLockShapeData** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceLockShapeData  <br/> |
   
Para obtener una referencia a la celda **ReplaceLockShapeData** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceLockShapeData** <br/> |
   

