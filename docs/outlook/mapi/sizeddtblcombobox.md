---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 39854c320078d2e2ca2365244f094e28962380d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593658"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura con nombre que incluye una estructura [DTBLCOMBOBOX](dtblcombobox.md) para describir un control de cuadro combinado y el número máximo de caracteres que se puede escribir en el control de edición asociado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Parámetros

_n_
  
> Número de caracteres que se pueden escribir en el cuadro combinado de control de edición. 
    
_s_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La macro **SizedDtblComboBox** le permite definir un cuadro combinado cuando se conoce la longitud de la cadena de caracteres habilitado. Se crea la nueva estructura con los siguientes miembros: 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

Para utilizar un puntero a la estructura resultante de la macro **SizedDtblComboBox** como un puntero de estructura **DTBLCOMBOBOX** , realizar la conversión a la siguiente: 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>Recursos adicionales

- [DTBLCOMBOBOX](dtblcombobox.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

