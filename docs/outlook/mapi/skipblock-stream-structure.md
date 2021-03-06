---
title: Estructura de secuencias SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435547"
---
# <a name="skipblock-stream-structure"></a>Estructura de secuencias SkipBlock

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una estructura de secuencia SkipBlock es un bloque de datos que comienza por un entero que especifica la longitud de la parte restante del bloque. Esta estructura de secuencia existe en un [flujo FieldDefinition](fielddefinition-stream-structure.md) si la definición de campo está en formato PropDefV2. 
  
El propósito de una estructura de secuencia SkipBlock depende de su ubicación relativa en una serie de estructuras similares en el elemento de datos SkipBlocks de una secuencia FieldDefinition. La serie SkipBlocks debe contener al menos una estructura SkipBlock que termine la serie y tenga el elemento de datos Size igual a 0. Si la primera estructura no es la estructura de terminación (es decir, el elemento de datos Size es mayor que 0), Outlook supone que la primera estructura especifica el nombre del campo en Unicode (UTF-16).
  
Los elementos de datos de esta secuencia se almacenan en el orden de bytes little-endian, siguiendo inmediatamente entre sí en el orden especificado a continuación.
  
- Size: DWORD (4 bytes), el tamaño, en número de bytes, del elemento de datos Content.
    
- Contenido: una matriz de BYTES. El recuento de esta matriz es igual al elemento de datos Size. El significado del elemento de datos Content depende de la ubicación de la estructura SkipBlock en la serie y de la versión de Outlook. Si la primera estructura SkipBlock no es la estructura de terminación, Outlook considera la primera estructura SkipBlock como la estructura de secuencia [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) que especifica el nombre del campo en Unicode. 
    
## <a name="see-also"></a>Vea también



[Outlook Elementos y campos](outlook-items-and-fields.md)
  
[Estructuras de secuencias](stream-structures.md)
  
[Estructura de secuencia FieldDefinition](fielddefinition-stream-structure.md)
  
[Estructura de secuencias FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

