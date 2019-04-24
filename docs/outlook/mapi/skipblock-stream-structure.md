---
title: Estructura de la secuencia SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282673"
---
# <a name="skipblock-stream-structure"></a>Estructura de la secuencia SkipBlock

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una estructura de secuencia SkipBlock es un bloque de datos que comienza con un entero que especifica la longitud de la parte restante del bloque. Esta estructura de secuencia existe en una secuencia [FieldDefinition](fielddefinition-stream-structure.md) si la definición del campo está en formato PropDefV2. 
  
El propósito de una estructura de secuencia SkipBlock depende de su ubicación relativa en una serie de estructuras like en el elemento de datos SkipBlocks de una secuencia FieldDefinition. La serie SkipBlocks debe contener al menos una estructura SkipBlock que finalice la serie y tenga el elemento de datos tamaño igual a 0. Si la primera estructura no es la estructura final (es decir, el elemento de datos size es mayor que 0), Outlook supone que la primera estructura especifica el nombre del campo en Unicode (UTF-16).
  
Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el orden especificado a continuación.
  
- Size: DWORD (4 bytes), el tamaño, en número de bytes, del elemento de datos de contenido.
    
- Content: una matriz de BYTEs. El recuento de esta matriz es igual al elemento de datos de tamaño. El significado del elemento de datos de contenido depende de la ubicación de la estructura SkipBlock en la serie y la versión de Outlook. Si la primera estructura SkipBlock no es la estructura de terminación, Outlook considera la primera estructura SkipBlock como la estructura de la secuencia [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) que especifica el nombre del campo en Unicode. 
    
## <a name="see-also"></a>Vea también



[Campos y elementos de Outlook](outlook-items-and-fields.md)
  
[Estructuras de secuencia](stream-structures.md)
  
[Estructura de la secuencia FieldDefinition](fielddefinition-stream-structure.md)
  
[Estructura de la secuencia FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

