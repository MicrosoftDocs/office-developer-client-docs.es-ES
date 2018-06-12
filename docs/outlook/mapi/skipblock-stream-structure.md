---
title: Estructura de la secuencia de SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: d84704300602bada4cf93c9d3f6622feaf16f352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820693"
---
# <a name="skipblock-stream-structure"></a>Estructura de la secuencia de SkipBlock

  
  
**Se aplica a**: Outlook 
  
Una estructura de secuencia de SkipBlock es un bloque de datos que comienza con un número entero que especifica la longitud de la parte restante del bloque. Esta estructura de secuencia existe en una secuencia [FieldDefinition](fielddefinition-stream-structure.md) si la definición de campo se encuentra en formato de PropDefV2. 
  
El propósito de una estructura de secuencia SkipBlock depende de la ubicación relativa en una serie de como estructuras en el elemento de datos de SkipBlocks de una secuencia FieldDefinition. La serie SkipBlocks debe contener al menos una estructura SkipBlock que finaliza la serie y que tenga el elemento de datos de tamaño igual a 0. Si la primera estructura no es la estructura de terminación (es decir, el elemento de datos de tamaño es mayor que 0), Outlook se da por supuesto que la primera estructura especifica el nombre del campo en Unicode (UTF-16).
  
Elementos de datos en esta secuencia se almacenan en orden de bytes little-endian, inmediatamente después de entre sí en el orden especificado a continuación.
  
- Tamaño: DWORD (4 bytes), el tamaño, en número de bytes, del elemento de datos de contenido.
    
- Contenido: Una matriz de bytes. El recuento de esta matriz es igual al elemento de datos de tamaño. El significado del elemento de datos de contenido depende de la ubicación de la estructura de SkipBlock en la serie y la versión de Outlook. Si la primera estructura SkipBlock no es la estructura de terminación, Outlook considera la primera estructura SkipBlock como la estructura de la secuencia de [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) que especifica el nombre del campo en Unicode. 
    
## <a name="see-also"></a>Ver también



[Campos y elementos de outlook](outlook-items-and-fields.md)
  
[Estructuras de secuencia](stream-structures.md)
  
[Estructura de secuencia FieldDefinition](fielddefinition-stream-structure.md)
  
[Estructura de la secuencia de FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

