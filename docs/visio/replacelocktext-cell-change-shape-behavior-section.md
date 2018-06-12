---
title: Celda ReplaceLockText (sección de comportamiento de cambio forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma. El ReplaceLockText determina si el texto que aparece en el maestro de sobrescribe el texto de la forma reemplazada.
ms.openlocfilehash: 75fb0831e7361345f04d7912eb0a55959d9417cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822989"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>Celda ReplaceLockText (sección de comportamiento de cambio forma)

Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma. El **ReplaceLockText** determina si el texto que aparece en el maestro de sobrescribe el texto de la forma reemplazada. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> | El texto en la forma de patrón sobrescribe el texto de la forma anterior. Además, la forma de patrón sobrescribe los valores de las celdas en las secciones siguientes durante una operación de reemplazo de forma:  <br/> Sección de **Campos de texto**  <br/> Sección **Text Block Format**  <br/> |
|FALSE  <br/> |La forma de reemplazo contiene cualquier texto, los campos de texto u otras propiedades de texto de la forma anterior que se han agregado a la forma.  <br/> Cuando la forma de reemplazo contiene las propiedades de texto de la forma anterior, la forma de reemplazo tiene también los valores de las secciones de **carácter** y de **párrafo** de la forma antigua si tienen más de una fila.  <br/> |
   
Si se establece en TRUE (1), los valores de la forma patrón reemplaza los valores de las siguientes opciones en la forma reemplazada:
  
- [Celda TheText (Sección de eventos)](thetext-cell-events-section.md)
    
- Celdas en la [sección de caracteres](character-section.md)
    
- Celdas en la [sección de párrafo](paragraph-section.md)
    
- Celdas en la [sección de tabulaciones](tabs-section.md)
    
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda **ReplaceLockText** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceLockText  <br/> |
   
Para obtener una referencia a la celda **ReplaceLockText** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceLockText** <br/> |
   

