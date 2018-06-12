---
title: Estructura de la secuencia de PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 5494558db65e19891848264c170ba85a55c5df71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818461"
---
# <a name="packedansistring-stream-structure"></a>Estructura de la secuencia de PackedAnsiString

  
  
**Se aplica a**: Outlook 
  
La estructura de la secuencia de PackedAnsiString contiene una representación ANSI de una cadena, en función de la página de códigos ANSI del equipo donde se ejecuta Microsoft Outlook. Esta cadena no termina con un carácter nulo. Elementos de datos en esta secuencia se almacenan en orden de bytes little-endian, inmediatamente después de entre sí en el orden indicado a continuación. Los elementos de datos reales que existen dependen de la longitud de la cadena de representación ANSI.
  
- Una cadena cuya representación ANSI contiene menos de 255 bytes, los elementos de datos son los siguientes:
    
  - Duración: Bytes (1 byte), la longitud, en número de bytes, de la representación ANSI de la cadena.
    
  - Caracteres: Una matriz de CHAR. El recuento de esta matriz es igual al elemento de datos de longitud. Los datos de la matriz están la representación ANSI de la cadena.
    
- Una cadena cuya representación ANSI contiene 255 a 65535 bytes, los elementos de datos son los siguientes:
    
  - Prefijo: Bytes (1 byte), el valor de 255 (0xff).
    
  - Duración: WORD (2 bytes), la longitud, en número de bytes, de la representación ANSI de la cadena.
    
  - Caracteres: Una matriz de CHAR. El recuento de esta matriz es igual al elemento de datos de longitud. Los datos de la matriz están la representación ANSI de la cadena.
    
## <a name="see-also"></a>Ver también



[Campos y elementos de outlook](outlook-items-and-fields.md)
  
[Estructuras de secuencia](stream-structures.md)
  
[Estructura de secuencia FieldDefinition](fielddefinition-stream-structure.md)

