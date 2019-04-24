---
title: Estructura de la secuencia PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348513"
---
# <a name="packedansistring-stream-structure"></a>Estructura de la secuencia PackedAnsiString

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La estructura de la secuencia PackedAnsiString contiene una representación ANSI de una cadena, basada en la página de códigos ANSI del equipo en el que se está ejecutando Microsoft Outlook. Esta cadena no termina con un carácter null. Los elementos de datos de esta secuencia se almacenan en el orden de bytes Little-endian, inmediatamente a continuación entre sí en el orden indicado a continuación. Los elementos de datos reales que existen dependen de la longitud de la cadena en la representación ANSI.
  
- En el caso de una cadena cuya representación ANSI contenga menos de 255 bytes, los elementos de datos serán los siguientes:
    
  - Longitud: BYTE (1 byte), longitud, en número de bytes, de la representación ANSI de la cadena.
    
  - Caracteres: una matriz de CHAR. El recuento de esta matriz es igual al elemento de datos de longitud. Los datos de la matriz son la representación ANSI de la cadena.
    
- Para una cadena cuya representación ANSI contiene de 255 a 65535 bytes, los elementos de datos son los siguientes:
    
  - Prefix: BYTE (1 byte), el valor de 255 (0xFF).
    
  - Longitud: WORD (2 bytes), la longitud, en número de bytes, de la representación ANSI de la cadena.
    
  - Caracteres: una matriz de CHAR. El recuento de esta matriz es igual al elemento de datos de longitud. Los datos de la matriz son la representación ANSI de la cadena.
    
## <a name="see-also"></a>Vea también



[Campos y elementos de Outlook](outlook-items-and-fields.md)
  
[Estructuras de secuencia](stream-structures.md)
  
[Estructura de la secuencia FieldDefinition](fielddefinition-stream-structure.md)

