---
title: Estructura de la secuencia PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fc20c259f30ded2f96f3bf314e74207bebcac980
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422617"
---
# <a name="packedunicodestring-stream-structure"></a>Estructura de la secuencia PackedUnicodeString

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La estructura de la secuencia PackedUnicodeString contiene una representación Unicode (UTF-16) de una cadena. Esta cadena no termina con un carácter null. Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el orden indicado a continuación. Los elementos de datos reales que existen dependen de la longitud de la cadena en la representación UTF-16.
  
- Para una cadena cuya representación UTF-16 contiene menos de 255 WCHARs, los elementos de datos son los siguientes:
    
  - Longitud: BYTE (1 byte), longitud, en número de WCHARs, de la representación UTF-16 de la cadena.
    
  - Caracteres: una matriz de WCHAR. El recuento de esta matriz es igual al elemento de datos de longitud. Los datos de la matriz son la representación UTF-16 de la cadena.
    
- Para una cadena cuya representación UTF-16 contiene de 255 a 65535 WCHARs, los elementos de datos son los siguientes:
    
  - Prefix: BYTE (1 byte), el valor de 255 (0xFF).
    
  - Longitud: WORD (2 bytes), la longitud, en número de WCHARs, de la representación UTF-16 de la cadena.
    
  - Caracteres: una matriz de WCHAR. El recuento de esta matriz es igual al elemento de datos de longitud. Los datos de la matriz son la representación UTF-16 de la cadena.
    
## <a name="see-also"></a>Ver también



[Campos y elementos de Outlook](outlook-items-and-fields.md)
  
[Estructuras de secuencia](stream-structures.md)
  
[Estructura de la secuencia FieldDefinition](fielddefinition-stream-structure.md)

