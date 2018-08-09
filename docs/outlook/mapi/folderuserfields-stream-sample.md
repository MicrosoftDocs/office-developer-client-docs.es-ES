---
title: Ejemplo de secuencia de FolderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 72c71a6109f55f7ec06499e214a1aa11292a9e52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816833"
---
# <a name="folderuserfields-stream-sample"></a>Ejemplo de secuencia de FolderUserFields

**Hace referencia a**: Outlook 
  
En este tema se describe un ejemplo de una secuencia de FolderUserFields. La secuencia contiene una definición de un campo definido por el usuario, `TextField1`. El tipo es **texto**, y la secuencia de FolderUserFields contiene los elementos FolderUserFieldsAnsi y FolderUserFieldsUnicode. Para obtener más información, vea [Estructuras de secuencia de los campos de carpeta](folder-fields-stream-structures.md).
  
## <a name="data-dump"></a>Volcado de datos

El siguiente es un volcado de datos de la secuencia tal y como se mostrarían en un editor binario.
  
|Desplazamiento de la secuencia|Bytes de datos|Datos ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

El siguiente es un análisis de los datos de ejemplo de la secuencia de **FolderUserFields** :
  
- FolderUserFieldsAnsi: Desplazamiento 0 x 0.
    
  - FieldDefinitionCount: Desplazamiento 0 x 0, 4 bytes: 0 x 00000002 (2).
    
  - FieldDefinitions: Desplazamiento 0 x 4, matriz de secuencias de FolderFieldDefinitionA 2.
    
    **Primer elemento de matriz**:
    
    - FieldType: Desplazamiento 0 x 4, 4 bytes: 0 x 00000001 (ftString).
      
    - FieldNameLength: Desplazamiento 0 x 8, 2 bytes: 0x000A (10)
      
    - FieldName: Desplazamiento 0xA, matriz de 10 caracteres. Valor de cadena ANSI: "TextField1".
      
    - Común: Desplazamiento 0 x 14.
    
      - PropSetGuid: Desplazamiento 0 x 14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: desplazamiento 0 x 24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: desplazamiento 0 x 28, 4 bytes: 0 x 00000000.
        
      - dwBitmap: desplazamiento 0x2C, 4 bytes: 0 x 00000000.
        
      - dwDisplay: desplazamiento 0 x 30, 4 bytes: 0 x 00000000.
        
      - iFmt: desplazamiento 0x34, 4 bytes: 0 x 00000000.
        
      - wszFormulaLength: 0x38, 2 bytes de desplazamiento: 0 x 0000 (0).
        
      - wszFormula: desplazamiento 0x3A, matriz de número de WCHAR 0. Valor de cadena vacía.
    
    **Segundo elemento de matriz**:
    
    - FieldType: Desplazamiento 0x3A, 4 bytes: 0 x 00000000 (ftNone).
      
    - FieldNameLength: Desplazamiento 0x3E, 2 bytes: 0 x 0000 (0).
      
    - FieldName: Desplazamiento 0 x 40, matriz de 0 caracteres. Valor de cadena vacía.
      
    - Común: Desplazamiento 0 x 40.
    
      - PropSetGuid: Desplazamiento 0 x 40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: desplazamiento 0 x 50, 4 bytes: 0 x 00000000 (0).
        
      - dwString: desplazamiento 0 x 54, 4 bytes: 0 x 00000000.
        
      - dwBitmap: desplazamiento 0 x 58, 4 bytes: 0 x 00000000.
        
      - dwDisplay: desplazamiento 0x5C, 4 bytes: 0 x 00000000.
        
      - iFmt: desplazamiento 0 x 60, 4 bytes: 0 x 00000000.
        
      - wszFormulaLength: 0x64, 2 bytes de desplazamiento: 0 x 0000 (0).
        
      - wszFormula: desplazamiento 0x66, matriz de número de WCHAR 0. Valor de cadena vacía.
    
- FolderUserFieldsUnicode: Desplazamiento 0x66.
    
  - FieldDefinitionCount: Desplazamiento 0x66, 4 bytes: 0 x 00000002 (2).
    
  - FieldDefinitions: Desplazamiento 0x6A, matriz de secuencias de FolderFieldDefinitionW 2.
    
    **Primer elemento de matriz**:
    
    - FieldType: Desplazamiento 0x6A, 4 bytes: 0 x 00000001 (ftString).
      
    - FieldNameLength: Desplazamiento 0x6E, 2 bytes: 0x000A (10).
      
    - FieldName: Desplazamiento 0 x 70, matriz de número de 10 WCHAR. Valor de cadena Unicode: "TextField1".
      
    - Común: Desplazamiento 0 x 84.
    
      - PropSetGuid: Desplazamiento 0 x 84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: desplazamiento 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: desplazamiento 0x98, 4 bytes: 0 x 00000000.
        
      - dwBitmap: desplazamiento 0x9C, 4 bytes: 0 x 00000000.
        
      - dwDisplay: desplazamiento 0xA0, 4 bytes: 0 x 00000000.
        
      - iFmt: desplazamiento 0xA4, 4 bytes: 0 x 00000000.
        
      - wszFormulaLength: 0xA8, 2 bytes de desplazamiento: 0 x 0000 (0).
        
      - wszFormula: desplazamiento 0xAA, matriz de número de WCHAR 0. Valor de cadena vacía.
    
    **Segundo elemento de matriz**:
    
    - FieldType: Desplazamiento 0xAA, 4 bytes: 0 x 00000000 (ftNone).
      
    - FieldNameLength: Desplazamiento 0xAE, 2 bytes: 0 x 0000 (0).
      
    - FieldName: Desplazamiento 0xB0, matriz de número de WCHAR 0. Valor de cadena vacía.
      
    - Común: Desplazamiento 0xB0.
    
      - PropSetGuid: Desplazamiento 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: desplazamiento 0xC0, 4 bytes: 0 x 00000000 (0).
        
      - dwString: desplazamiento 0xC4, 4 bytes: 0 x 00000000.
        
      - dwBitmap: desplazamiento 0xC8, 4 bytes: 0 x 00000000.
        
      - dwDisplay: desplazamiento 0xCC, 4 bytes: 0 x 00000000.
        
      - iFmt: desplazamiento 0xD0, 4 bytes: 0 x 00000000.
        
      - wszFormulaLength: desplazamiento 0xD4, 2 bytes: 0 x 0000 (0).
        
      - wszFormula: desplazamiento 0xD6, matriz de número de WCHAR 0. Valor de cadena vacía.
    
## <a name="see-also"></a>Vea también

- [Campos y elementos de Outlook](outlook-items-and-fields.md)
- [Muestra de la secuencia PropertyDefinition](propertydefinition-stream-structure.md)
- [Muestra de la secuencia FieldDefinition](fielddefinition-stream-structure.md)
- [Estructura de la secuencia SkipBlock](skipblock-stream-structure.md)
- [Estructura de la secuencia FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Estructura de la secuencia PackedAnsiString](packedansistring-stream-structure.md)
- [Estructura de la secuencia PackedUnicodeString](packedunicodestring-stream-structure.md)

