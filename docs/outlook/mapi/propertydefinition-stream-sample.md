---
title: Ejemplo de secuencia de PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3d0c337bd3e5a73bbbcbb72a109320cfb84efd50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820460"
---
# <a name="propertydefinition-stream-sample"></a>Ejemplo de secuencia de PropertyDefinition

**Se aplica a**: Outlook 
  
En este tema se describe un ejemplo de una secuencia de PropertyDefinition. La secuencia contiene una definición de un campo definido por el usuario, `TextField1`. El tipo es **texto**, y la definición de está en el formato PropDefV2.
  
## <a name="data-dump"></a>Volcado de datos

El siguiente es un volcado de datos de la secuencia tal y como se mostrarían en un editor binario.
  
|Desplazamiento de la secuencia|Bytes de datos|Datos ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
El siguiente es un análisis de los datos de ejemplo de la secuencia de PropertyDefinition:
  
- Versión: Desplazamiento 0 x 0, 2 bytes: 0 x 0103 (PropDefV2).
    
- FieldDefinitionCount: Desplazamiento 0 x 2, 4 bytes: 0 x 1 (1).
    
- FieldDefinitions: Desplazamiento 0 x 6, matriz de secuencia de FieldDefinition 1.
    
  - Indicadores: Desplazamiento 0 x 6, 4 bytes: 0 x 45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).
    
  - VT: Desplazamiento 0xA, 2 bytes: 0 x 8 (**VT_BSTR**).
    
  - DispId: Desplazamiento 0xC, 4 bytes: 0 x 0 (0).
    
  - NmidNameLength: Desplazamiento 0 x 10, 2 bytes: 0xA (10).
    
  - NmidName: Desplazamiento 0 x 12, matriz de número de 10 WCHAR. Valor de cadena Unicode: "TextField1".
    
  - NameANSI: Desplazamiento 0 x 26, PackedAnsiString secuencia.
    
    - Duración: Desplazamiento 0 x 26, 1 byte: 0xA (10).
      
    - Caracteres: Desplazamiento 0 x 27, matriz de 10 caracteres. Valor de cadena ANSI: "TextField1".
    
  - FormulaANSI: Desplazamiento 0 x 31, PackedAnsiString secuencia.
    
    - Duración: Desplazamiento 0 x 31, 1 byte: 0 x 0 (0).
      
    - Caracteres: Desplazamiento 0 x 32, matriz de 0 caracteres. Cadena ANSI vacía.
    
  - ValidationRuleANSI: Desplazamiento 0 x 32, PackedAnsiString secuencia.
    
    - Duración: Desplazamiento 0 x 32, 1 byte: 0 x 0 (0).
      
    - Caracteres: Desplazamiento 0 x 33, matriz de 0 caracteres. Cadena ANSI vacía.
    
  - ValidationTextANSI: Desplazamiento 0 x 33, PackedAnsiString secuencia.
    
    - Duración: Desplazamiento 0 x 33, 1 byte: 0 x 0 (0).
      
    - Caracteres: Desplazamiento 0x34, matriz de 0 caracteres. Cadena ANSI vacía.
    
  - ErrorANSI: Desplazamiento 0x34, PackedAnsiString secuencia.
    
    - Duración: Desplazamiento 0x34, 1 byte: 0 x 0 (0).
      
    - Caracteres: Desplazamiento 0x35, matriz de 0 caracteres. Cadena ANSI vacía.
    
  - InternalType: Desplazamiento 0x35, 4 bytes: 0 x 0 (iTypeString).
    
  - SkipBlocks: Desplazamiento 0 x 39, serie de secuencias de SkipBlock.
    
  - Primera SkipBlock
    
    - Tamaño: Desplazamiento 0 x 39, 4 bytes: 0x15 (21).
      
    - Contenido: Desplazamiento 0x3D, matriz de bytes 21. Esta es la primera secuencia de SkipBlock, por lo que esta matriz contiene una secuencia de FirstSkipBlockContent.
      
      - FieldName: Desplazamiento 0x3D, PackedUnicodeString secuencia.
        
        - Duración: Desplazamiento 0x3D, 1 byte: 0xA (10).
          
        - Caracteres: Desplazamiento 0x3E, matriz de número de 10 WCHAR. Valor de cadena Unicode: "TextField1".
    
  - Segundo SkipBlock
    
    - Tamaño: Desplazamiento 0 x 52, 4 bytes: 0 x 0 (0). Esta es la secuencia de SkipBlock terminación.
    
## <a name="see-also"></a>Ver también

- [Campos y elementos de outlook](outlook-items-and-fields.md)
- [Estructuras de secuencia](stream-structures.md)
- [Estructura de la secuencia de PropertyDefinition](propertydefinition-stream-structure.md)
- [Estructura de secuencia FieldDefinition](fielddefinition-stream-structure.md)
- [Estructura de la secuencia de SkipBlock](skipblock-stream-structure.md)
- [Estructura de la secuencia de FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Estructura de la secuencia de PackedAnsiString](packedansistring-stream-structure.md)
- [Estructura de la secuencia de PackedUnicodeString](packedunicodestring-stream-structure.md)

