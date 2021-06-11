---
title: Estructura de secuencias PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404508"
---
# <a name="packedansistring-stream-structure"></a>Estructura de secuencias PackedAnsiString

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La estructura de secuencia PackedAnsiString contiene una representación ANSI de una cadena, basada en la página de código ANSI del equipo en el que se ejecuta Microsoft Outlook. Esta cadena no termina con un carácter nulo. Los elementos de datos de esta secuencia se almacenan en orden de bytes little-endian, siguiendo inmediatamente entre sí en el orden que se muestra a continuación. Los elementos de datos reales que existen dependen de la longitud de la cadena en la representación ANSI.
  
- Para una cadena cuya representación ANSI contiene menos de 255 bytes, los elementos de datos son los siguientes:
    
  - Length: BYTE (1 byte), la longitud, en número de bytes, de la representación ANSI de la cadena.
    
  - Caracteres: una matriz de CHAR. El recuento de esta matriz es igual al elemento de datos Length. Los datos de la matriz son la representación ANSI de la cadena.
    
- Para una cadena cuya representación ANSI contiene de 255 a 65535 bytes, los elementos de datos son los siguientes:
    
  - Prefijo: BYTE (1 byte), el valor de 255 (0xff).
    
  - Length: WORD (2 bytes), la longitud, en número de bytes, de la representación ANSI de la cadena.
    
  - Caracteres: una matriz de CHAR. El recuento de esta matriz es igual al elemento de datos Length. Los datos de la matriz son la representación ANSI de la cadena.
    
## <a name="see-also"></a>Vea también



[Outlook Elementos y campos](outlook-items-and-fields.md)
  
[Estructuras de secuencias](stream-structures.md)
  
[Estructura de secuencia FieldDefinition](fielddefinition-stream-structure.md)

