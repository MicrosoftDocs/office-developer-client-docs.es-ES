---
title: Estructura de la secuencia PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4e919270efb196cda845581830cc4a918012b385
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578979"
---
# <a name="packedansistring-stream-structure"></a>Estructura de la secuencia PackedAnsiString

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La estructura de la secuencia de PackedAnsiString contiene una representación ANSI de una cadena, en función de la página de códigos ANSI del equipo donde se ejecuta Microsoft Outlook. Esta cadena no termina con un carácter nulo. Elementos de datos en esta secuencia se almacenan en orden de bytes little-endian, inmediatamente después de entre sí en el orden indicado a continuación. Los elementos de datos reales que existen dependen de la longitud de la cadena de representación ANSI.
  
- Una cadena cuya representación ANSI contiene menos de 255 bytes, los elementos de datos son los siguientes:
    
  - Duración: Bytes (1 byte), la longitud, en número de bytes, de la representación ANSI de la cadena.
    
  - Caracteres: Una matriz de CHAR. El recuento de esta matriz es igual al elemento de datos de longitud. Los datos de la matriz están la representación ANSI de la cadena.
    
- Una cadena cuya representación ANSI contiene 255 a 65535 bytes, los elementos de datos son los siguientes:
    
  - Prefijo: Bytes (1 byte), el valor de 255 (0xff).
    
  - Duración: WORD (2 bytes), la longitud, en número de bytes, de la representación ANSI de la cadena.
    
  - Caracteres: Una matriz de CHAR. El recuento de esta matriz es igual al elemento de datos de longitud. Los datos de la matriz están la representación ANSI de la cadena.
    
## <a name="see-also"></a>Recursos adicionales



[Campos y elementos de Outlook](outlook-items-and-fields.md)
  
[Estructuras de secuencia](stream-structures.md)
  
[Muestra de la secuencia FieldDefinition](fielddefinition-stream-structure.md)

