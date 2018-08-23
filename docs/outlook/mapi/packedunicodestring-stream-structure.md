---
title: Estructura de la secuencia PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 00791ab47cc3c6bd435d6f581e5ada53ae59d73b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569200"
---
# <a name="packedunicodestring-stream-structure"></a>Estructura de la secuencia PackedUnicodeString

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La estructura de la secuencia de PackedUnicodeString contiene una representación Unicode (UTF-16) de una cadena. Esta cadena no termina con un carácter nulo. Elementos de datos en esta secuencia se almacenan en orden de bytes little-endian, inmediatamente después de entre sí en el orden indicado a continuación. Los elementos de datos reales que existen dependen de la longitud de la cadena de representación UTF-16.
  
- Una cadena cuya representación UTF-16 contiene el número de WCHAR menor que 255, los elementos de datos son los siguientes:
    
  - Duración: Bytes (1 byte), la longitud, en número de número de WCHAR, de la representación UTF-16 de la cadena.
    
  - Caracteres: Una matriz de WCHAR. El recuento de esta matriz es igual al elemento de datos de longitud. Los datos de la matriz están la representación UTF-16 de la cadena.
    
- Una cadena cuya representación UTF-16 contiene el número de 255 a 65535 WCHAR, los elementos de datos son los siguientes:
    
  - Prefijo: Bytes (1 byte), el valor de 255 (0xff).
    
  - Duración: WORD (2 bytes), la longitud, en número de número de WCHAR, de la representación UTF-16 de la cadena.
    
  - Caracteres: Una matriz de WCHAR. El recuento de esta matriz es igual al elemento de datos de longitud. Los datos de la matriz están la representación UTF-16 de la cadena.
    
## <a name="see-also"></a>Recursos adicionales



[Campos y elementos de Outlook](outlook-items-and-fields.md)
  
[Estructuras de secuencia](stream-structures.md)
  
[Muestra de la secuencia FieldDefinition](fielddefinition-stream-structure.md)

