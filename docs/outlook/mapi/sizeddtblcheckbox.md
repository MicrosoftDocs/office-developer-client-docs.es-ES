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
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420811"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura con nombre que incluye una [estructura DTBLCHECKBOX](dtblcheckbox.md) para describir un control de casilla y una etiqueta de una longitud especificada. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionada:  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>Parameters

_n_
  
> Longitud de la etiqueta que se incluirá en la nueva estructura.
    
_s_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La **macro SizedDtblCheckBox** permite definir una casilla cuando se conoce el número de caracteres de etiqueta. La nueva estructura se crea con los siguientes miembros: 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

Para usar un puntero a la estructura resultante de la macro **SizedDtblCheckBox** como puntero de **estructura DTBLCHECKBOX,** realice la conversión siguiente: 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>Vea también

- [DTBLCHECKBOX](dtblcheckbox.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

