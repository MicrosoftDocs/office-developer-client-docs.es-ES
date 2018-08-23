---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6120439ea0d98ed6b64fe1542a4372265574723a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567534"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura con nombre que incluye una estructura [DTBLCHECKBOX](dtblcheckbox.md) para describir un control de casilla de verificación y una etiqueta de un período especificado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>Parámetros

_n_
  
> Longitud de la etiqueta que se deben incluir en la nueva estructura.
    
_s_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La macro **SizedDtblCheckBox** le permite definir una casilla de verificación cuando se conoce el número de caracteres de la etiqueta. Se crea la nueva estructura con los siguientes miembros: 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

Para utilizar un puntero a la estructura resultante de la macro **SizedDtblCheckBox** como un puntero de estructura **DTBLCHECKBOX** , realizar la conversión a la siguiente: 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>Recursos adicionales

- [DTBLCHECKBOX](dtblcheckbox.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

