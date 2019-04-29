---
title: Celda ReplaceLockFormat (sección cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma. Si la celda ReplaceLockFormat de una forma de patrón se establece en TRUE (1), los valores de formato del patrón sobrescribirán todos los valores correspondientes de una forma que sea reemplazado por el patrón.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427237"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>Celda ReplaceLockFormat (sección cambiar comportamiento de forma)

Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma que se reemplaza durante una operación de reemplazo de forma. Si la celda **ReplaceLockFormat** de una forma de patrón se establece en true (1), los valores de formato del patrón sobrescribirán todos los valores correspondientes de una forma que sea reemplazado por el patrón. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Si la celda **ReplaceLockFormat** de una forma de patrón está establecida en true, los valores de formato del patrón sobrescribirán todos los valores correspondientes de una forma que sea reemplazado por el patrón.  <br/> |
|FALSE  <br/> |Si la celda **ReplaceLockFormat** de una forma de patrón está establecida en false, la nueva forma de reemplazo contiene los valores de formato local de la forma antigua después de la operación de reemplazo.  <br/> |
   
## <a name="remarks"></a>Comentarios

La celda **ReplaceLockFormat** determina si la forma de patrón sobrescribirá los valores de formato local de las celdas de las siguientes secciones durante una operación de reemplazo de formas: 
  
- Sección de **formato de relleno** 
    
- Sección de **formato de línea** 
    
- Sección de **estilo rápido** 
    
- Sección **propiedades del tema** 
    
- Sección **propiedades** de degradado 
    
- Sección **propiedades de bisel** 
    
- Sección **propiedades del efecto adicional** 
    
- Sección degradado de **línea en puntos** 
    
- Sección de delimitadores de **relleno** 
    
Para obtener una referencia a la celda **ReplaceLockFormat** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceLockFormat  <br/> |
   
Para obtener una referencia desde un programa a la celda **ReplaceLockFormat** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceLockFormat** <br/> |
   

