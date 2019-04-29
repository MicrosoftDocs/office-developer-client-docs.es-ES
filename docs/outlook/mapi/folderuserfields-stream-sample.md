---
title: Ejemplo de secuencia FolderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5251a619c70221987847830897ba349d63fd9cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433979"
---
# <a name="folderuserfields-stream-sample"></a>Ejemplo de secuencia FolderUserFields

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se describe un ejemplo de una secuencia FolderUserFields. La secuencia contiene una definición de un campo definido por el usuario `TextField1`,. El tipo es **Text**y la secuencia FolderUserFields contiene tanto elementos FolderUserFieldsAnsi como FolderUserFieldsUnicode. Para obtener más información, vea las [estructuras de secuencia de campos de carpeta](folder-fields-stream-structures.md).
  
## <a name="data-dump"></a>Volcado de datos

El siguiente es un volcado de datos de la secuencia tal como se mostraría en un editor binario.
  
|Desplazamiento de secuencia|Bytes de datos|Datos ASCII|
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
   

A continuación se muestra un análisis de los datos de ejemplo para la secuencia **FolderUserFields** :
  
- FolderUserFieldsAnsi: desplazamiento 0X0.
    
  - FieldDefinitionCount: Offset 0X0, 4 bytes: 0x00000002 (2).
    
  - FieldDefinitions: desplazamiento 0x4, matriz de 2 secuencias de FolderFieldDefinitionA.
    
    **Primer elemento**de la matriz:
    
    - FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).
      
    - FieldNameLength: desplazamiento 0x8, 2 bytes: 0x000A (10)
      
    - FieldName: Offset 0xA, matriz de 10 caracteres. Valor de cadena ANSI: "TextField1".
      
    - Común: desplazamiento 0x14.
    
      - PropSetGuid: desplazamiento 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: desplazamiento 0x28, 4 bytes: 0x00000000.
        
      - dwBitmap: desplazamiento 0x2C, 4 bytes: 0x00000000.
        
      - dwDisplay: desplazamiento 0x30, 4 bytes: 0x00000000.
        
      - iFmt: desplazamiento 0x34, 4 bytes: 0x00000000.
        
      - wszFormulaLength: desplazamiento 0x38, 2 bytes: 0x0000 (0).
        
      - wszFormula: Offset 0x3A, matriz de 0 WCHARs. Valor de cadena vacía.
    
    **Segundo elemento**de la matriz:
    
    - FieldType: desplazamiento 0x3A, 4 bytes: 0x00000000 (ftNone).
      
    - FieldNameLength: desplazamiento 0x3E, 2 bytes: 0x0000 (0).
      
    - FieldName: PosiciónInicial 0x40, matriz de 0 caracteres. Valor de cadena vacía.
      
    - Común: desplazamiento 0x40.
    
      - PropSetGuid: desplazamiento 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: desplazamiento 0x50, 4 bytes: 0x00000000 (0).
        
      - dwString: desplazamiento 0x54, 4 bytes: 0x00000000.
        
      - dwBitmap: desplazamiento 0x58, 4 bytes: 0x00000000.
        
      - dwDisplay: desplazamiento 0x5C, 4 bytes: 0x00000000.
        
      - iFmt: desplazamiento 0x60, 4 bytes: 0x00000000.
        
      - wszFormulaLength: desplazamiento 0x64, 2 bytes: 0x0000 (0).
        
      - wszFormula: Offset 0x66, matriz de 0 WCHARs. Valor de cadena vacía.
    
- FolderUserFieldsUnicode: desplazamiento 0x66.
    
  - FieldDefinitionCount: desplazamiento 0x66, 4 bytes: 0x00000002 (2).
    
  - FieldDefinitions: Offset 0x6A, matriz de 2 secuencias de FolderFieldDefinitionW.
    
    **Primer elemento**de la matriz:
    
    - FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).
      
    - FieldNameLength: desplazamiento 0x6E, 2 bytes: 0x000A (10).
      
    - FieldName: Offset 0X70, matriz de 10 WCHARs. Valor de cadena Unicode: "TextField1".
      
    - Común: desplazamiento 0x84.
    
      - PropSetGuid: desplazamiento 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: desplazamiento 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: desplazamiento 0x98, 4 bytes: 0x00000000.
        
      - dwBitmap: desplazamiento 0x9C, 4 bytes: 0x00000000.
        
      - dwDisplay: desplazamiento 0xA0, 4 bytes: 0x00000000.
        
      - iFmt: desplazamiento 0xA4, 4 bytes: 0x00000000.
        
      - wszFormulaLength: desplazamiento 0xA8, 2 bytes: 0x0000 (0).
        
      - wszFormula: Offset 0xAA, matriz de 0 WCHARs. Valor de cadena vacía.
    
    **Segundo elemento**de la matriz:
    
    - FieldType: desplazamiento 0xAA, 4 bytes: 0x00000000 (ftNone).
      
    - FieldNameLength: desplazamiento 0xAE, 2 bytes: 0x0000 (0).
      
    - FieldName: Offset 0xB0, matriz de 0 WCHARs. Valor de cadena vacía.
      
    - Común: desplazamiento 0xB0.
    
      - PropSetGuid: desplazamiento 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: desplazamiento 0xC0, 4 bytes: 0x00000000 (0).
        
      - dwString: desplazamiento 0xC4, 4 bytes: 0x00000000.
        
      - dwBitmap: desplazamiento 0xC8, 4 bytes: 0x00000000.
        
      - dwDisplay: desplazamiento 0xCC, 4 bytes: 0x00000000.
        
      - iFmt: desplazamiento 0xD0, 4 bytes: 0x00000000.
        
      - wszFormulaLength: desplazamiento 0xD4, 2 bytes: 0x0000 (0).
        
      - wszFormula: Offset 0xD6, matriz de 0 WCHARs. Valor de cadena vacía.
    
## <a name="see-also"></a>Ver también

- [Campos y elementos de Outlook](outlook-items-and-fields.md)
- [Estructura de la secuencia PropertyDefinition](propertydefinition-stream-structure.md)
- [Estructura de la secuencia FieldDefinition](fielddefinition-stream-structure.md)
- [Estructura de la secuencia SkipBlock](skipblock-stream-structure.md)
- [Estructura de la secuencia FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Estructura de la secuencia PackedAnsiString](packedansistring-stream-structure.md)
- [Estructura de la secuencia PackedUnicodeString](packedunicodestring-stream-structure.md)

