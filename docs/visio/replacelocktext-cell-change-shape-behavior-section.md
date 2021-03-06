---
title: Celda ReplaceLockText (sección Cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de formas. ReplaceLockText determina si el texto que se muestra en el patrón sobrescribe el texto de la forma que se va a reemplazar.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411921"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>Celda ReplaceLockText (sección Cambiar comportamiento de forma)

Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de formas. **ReplaceLockText** determina si el texto que se muestra en el patrón sobrescribe el texto de la forma que se va a reemplazar. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> | El texto de la forma maestra sobrescribe el texto de la forma antigua. Además, la forma maestra sobrescribe los valores de las celdas de las secciones siguientes durante una operación de reemplazo de formas:  <br/> **Sección Campos de** texto  <br/> **Sección Formato de bloque de** texto  <br/> |
|FALSE  <br/> |La forma de reemplazo contiene cualquier texto, campos de texto u otras propiedades de texto de la forma antigua que se han agregado a la forma.  <br/> Cuando la forma de reemplazo contiene propiedades de texto de la  forma  antigua, la forma de reemplazo también tiene los valores de las secciones Carácter y Párrafo de la forma antigua si tienen más de una fila.  <br/> |
   
Si se establece en TRUE (1), los valores de la forma Master reemplazan los valores de lo siguiente en la forma que se va a reemplazar:
  
- [Celda TheText (Sección de eventos)](thetext-cell-events-section.md)
    
- Celdas de la [sección Carácter](character-section.md)
    
- Celdas de la [sección Párrafo](paragraph-section.md)
    
- Celdas de la [sección Pestañas](tabs-section.md)
    
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **ReplaceLockText** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la **propiedad CellsU,** use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceLockText  <br/> |
   
Para obtener una referencia desde un programa a la celda **ReplaceLockText** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceLockText** <br/> |
   

