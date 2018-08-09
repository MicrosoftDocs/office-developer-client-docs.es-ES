---
title: Celda ReplaceLockFormat (sección Cambiar comportamiento de forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma. Si la celda ReplaceLockFormat de una forma de patrón se establece en TRUE (1), los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que se reemplaza por el patrón.
ms.openlocfilehash: bf1e28353cc1e2d737a7d7a6dcd90caf14e19dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822956"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>Celda ReplaceLockFormat (sección Cambiar comportamiento de forma)

Indica si los valores de las celdas especificadas en una forma de patrón sobrescribirán los valores (incluidos los valores locales) de una forma reemplazada durante una operación de reemplazo de la forma. Si la celda **ReplaceLockFormat** de una forma de patrón se establece en TRUE (1), los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que se reemplaza por el patrón. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Si la celda **ReplaceLockFormat** de una forma de patrón está establecida en TRUE, los valores de formato del patrón sobrescriben todos los valores correspondientes de una forma que se reemplaza por el patrón.  <br/> |
|FALSE  <br/> |Si la celda **ReplaceLockFormat** de una forma de patrón se establece en FALSE, la forma de reemplazo contiene los valores de formato locales de la forma antigua después de la operación de reemplazo.  <br/> |
   
## <a name="remarks"></a>Comentarios

La celda **ReplaceLockFormat** determina si la forma de patrón sobrescribe los valores de formato locales de las celdas en las secciones siguientes durante una operación de reemplazo de forma: 
  
- Sección de **Formato de relleno** 
    
- Sección de **Formato de línea** 
    
- Sección de **Estilos rápidos** 
    
- Sección de **Propiedades del tema** 
    
- Sección de **Propiedades de degradado** 
    
- Sección de **Propiedades de bisel** 
    
- Sección de **Propiedades de efecto adicionales** 
    
- Sección de **Puntos de degradado en línea** 
    
- Sección de **Puntos de degradado de relleno** 
    
Para obtener una referencia a la celda **ReplaceLockFormat** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ReplaceLockFormat  <br/> |
   
Para obtener una referencia a la celda **ReplaceLockFormat** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowReplaceBehaviors** <br/> |
| Índice de celda:  <br/> |**visReplaceLockFormat** <br/> |
   

