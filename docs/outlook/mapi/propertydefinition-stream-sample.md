---
title: Ejemplo de secuencia PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406664"
---
# <a name="propertydefinition-stream-sample"></a>Ejemplo de secuencia PropertyDefinition

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se describe un ejemplo de una secuencia PropertyDefinition. La secuencia contiene una definición de un campo definido por el usuario `TextField1`,. El tipo es **Text**y la definición está en el formato PropDefV2.
  
## <a name="data-dump"></a>Volcado de datos

El siguiente es un volcado de datos de la secuencia tal como se mostraría en un editor binario.
  
|Desplazamiento de secuencia|Bytes de datos|Datos ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
A continuación se muestra un análisis de los datos de ejemplo para la secuencia PropertyDefinition:
  
- Versión: desplazamiento 0X0, 2 bytes: 0x0103 (PropDefV2).
    
- FieldDefinitionCount: desplazamiento 0X2, 4 bytes: 0x1 (1).
    
- FieldDefinitions: Offset 0x6, array de 1 FieldDefinition Stream.
    
  - Indicadores: DESREF 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).
    
  - VT: desplazamiento 0xA, 2 bytes: 0x8 (**VT_BSTR**).
    
  - DispId: Offset 0xC, 4 bytes: 0X0 (0).
    
  - NmidNameLength: DESREF 0x10, 2 bytes: 0xA (10).
    
  - NmidName: Offset 0X12, matriz de 10 WCHARs. Valor de cadena Unicode: "TextField1".
    
  - NameANSI: Offset 0x26, PackedAnsiString Stream.
    
    - Duración: desplazamiento 0x26, 1 byte: 0xA (10).
      
    - Caracteres: DESREF 0x27, matriz de 10 caracteres. Valor de cadena ANSI: "TextField1".
    
  - FormulaANSI: Offset 0x31, PackedAnsiString Stream.
    
    - Duración: desplazamiento 0x31, 1 byte: 0X0 (0).
      
    - Caracteres: desplazamiento bajo, matriz de 0 caracteres. Cadena ANSI vacía.
    
  - ValidationRuleANSI: Offset PackedAnsiString, Stream.
    
    - Longitud: desplaz. 1 byte: 0X0 (0).
      
    - Caracteres: Offset 0x33, matriz de 0 caracteres. Cadena ANSI vacía.
    
  - ValidationTextANSI: Offset 0x33, PackedAnsiString Stream.
    
    - Duración: desplazamiento 0x33, 1 byte: 0X0 (0).
      
    - Caracteres: Offset 0x34, matriz de 0 caracteres. Cadena ANSI vacía.
    
  - ErrorANSI: Offset 0x34, PackedAnsiString Stream.
    
    - Duración: desplazamiento 0x34, 1 byte: 0X0 (0).
      
    - Caracteres: Offset 0x35, matriz de 0 caracteres. Cadena ANSI vacía.
    
  - InternalType: desplazamiento 0x35, 4 bytes: 0X0 (iTypeString).
    
  - SkipBlocks: Offset 0x39, serie de secuencias de SkipBlock.
    
  - Primera SkipBlock
    
    - Tamaño: desplazamiento 0x39, 4 bytes: 0x15 (21).
      
    - Content: Offset 0x3D, matriz de 21 bytes. Esta es la primera secuencia SkipBlock, por lo que esta matriz contiene una secuencia FirstSkipBlockContent.
      
      - FieldName: Offset 0x3D, PackedUnicodeString Stream.
        
        - Duración: desplazamiento 0x3D, 1 byte: 0xA (10).
          
        - Caracteres: Offset 0x3E, matriz de 10 WCHARs. Valor de cadena Unicode: "TextField1".
    
  - Segundo SkipBlock
    
    - Size: DESREF 0x52, 4 bytes: 0X0 (0). Esta es la secuencia SkipBlock de terminación.
    
## <a name="see-also"></a>Ver también

- [Campos y elementos de Outlook](outlook-items-and-fields.md)
- [Estructuras de secuencia](stream-structures.md)
- [Estructura de la secuencia PropertyDefinition](propertydefinition-stream-structure.md)
- [Estructura de la secuencia FieldDefinition](fielddefinition-stream-structure.md)
- [Estructura de la secuencia SkipBlock](skipblock-stream-structure.md)
- [Estructura de la secuencia FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Estructura de la secuencia PackedAnsiString](packedansistring-stream-structure.md)
- [Estructura de la secuencia PackedUnicodeString](packedunicodestring-stream-structure.md)

