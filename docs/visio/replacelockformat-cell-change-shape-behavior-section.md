---
title: Celda ReplaceLockFormat (sección Cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de formas. Si la celda ReplaceLockFormat de una forma maestra está establecida en TRUE (1), los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que va a reemplazar el patrón.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427237"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>Celda ReplaceLockFormat (sección Cambiar comportamiento de forma)

Indica si los valores de las celdas especificadas en una forma maestra sobrescriben los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de formas. Si la **celda ReplaceLockFormat** de una forma maestra está establecida en TRUE (1), los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que va a reemplazar el patrón. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Si la **celda ReplaceLockFormat** de una forma maestra se establece en TRUE, los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que va a reemplazar el patrón.  <br/> |
|FALSE  <br/> |Si la **celda ReplaceLockFormat** de una forma maestra está establecida en FALSE, la forma de reemplazo contiene los valores de formato locales de la forma antigua después de la operación de reemplazo.  <br/> |
   
## <a name="remarks"></a>Comentarios

La **celda ReplaceLockFormat** determina si la forma maestra sobrescribe los valores de formato locales de las celdas de las secciones siguientes durante una operación de reemplazo de formas: 
  
- **Sección Formato de** relleno 
    
- **Sección Formato de** línea 
    
- **Sección Estilo** rápido 
    
- **Sección Propiedades del** tema 
    
- **Sección Propiedades de** degradado 
    
- **Sección Propiedades de biselado** 
    
- **Sección Propiedades de efecto adicionales** 
    
- **Sección De paradas de degradado de** línea 
    
- **Sección Fill Gradient Stops** 
    
Para obtener una referencia a la celda **ReplaceLockFormat** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceLockFormat  <br/> |
   
Para obtener una referencia desde un programa a la celda **ReplaceLockFormat** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceLockFormat** <br/> |
   

