---
title: Celda ReplaceLockText (sección cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma. ReplaceLockText determina si el texto que se muestra en el patrón sobrescribe el texto de la forma que se va a reemplazar.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348205"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>Celda ReplaceLockText (sección cambiar comportamiento de forma)

Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma. **ReplaceLockText** determina si el texto que se muestra en el patrón sobrescribe el texto de la forma que se va a reemplazar. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> | El texto de la forma patrón sobrescribirá el texto de la forma antigua. Además, la forma de patrón sobrescribe los valores de las celdas de las siguientes secciones durante una operación de reemplazo de formas:  <br/> Sección de **campos de texto**  <br/> Sección **formato del bloque de texto**  <br/> |
|FALSE  <br/> |La forma de reemplazo contiene cualquier texto, campos de texto u otras propiedades de texto de la forma antigua que se hayan agregado a la forma.  <br/> Cuando la forma de reemplazo contiene propiedades de texto de la forma antigua, la nueva forma de reemplazo también tiene los valores de las secciones de **carácter** y de **párrafo** de la forma antigua si tienen más de una fila.  <br/> |
   
Si se establece en TRUE (1), los valores de la forma principal reemplazan los valores de los siguientes en la forma que se está reemplazando:
  
- [Celda TheText (Sección de eventos)](thetext-cell-events-section.md)
    
- Celdas de la [sección de caracteres](character-section.md)
    
- Celdas de la [sección de párrafo](paragraph-section.md)
    
- Celdas de la [sección](tabs-section.md) de tabulaciones
    
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **ReplaceLockText** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceLockText  <br/> |
   
Para obtener una referencia desde un programa a la celda **ReplaceLockText** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceLockText** <br/> |
   

