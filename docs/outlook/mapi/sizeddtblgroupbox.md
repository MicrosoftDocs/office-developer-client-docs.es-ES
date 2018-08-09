---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a3d8a76905aa9abb0e5bf001688608e03446704a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820682"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**Hace referencia a**: Outlook 
  
Crea una estructura con nombre que incluye una estructura [DTBLGROUPBOX](dtblgroupbox.md) para describir un control de cuadro de grupo y una etiqueta de un período especificado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>Parámetros

_n_
  
> Longitud de etiqueta del cuadro de grupo. 
    
_s_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La macro **SizedDtblGroupBox** le permite definir un control de cuadro de grupo cuando se conoce la longitud de la etiqueta. Se crea la nueva estructura con los siguientes miembros: 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

Para utilizar un puntero a la estructura resultante de la macro **SizedDtblGroupBox** como un puntero de estructura **DTBLGROUPBOX** , realizar la conversión a la siguiente: 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>Vea también

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

