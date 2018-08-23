---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e50589b52f3e99bf2569a55bb7d3ca4f8247fd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591663"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura con nombre que incluye una estructura [DTBLEDIT](dtbledit.md) para describir un control de edición y el número máximo de caracteres que se puede escribir en el control. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Estructura relacionado:  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Parámetros

_n_
  
> Número máximo de caracteres que se puede escribir en el control de edición.
    
_s_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La macro **SizedDtblEdit** le permite definir un control de edición cuando se conoce el número de caracteres habilitados. Se crea la nueva estructura con los siguientes miembros: 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Para utilizar un puntero a la estructura resultante de la macro **SizedDtblEdit** como un puntero de estructura **DTBLEDIT** , realizar la conversión a la siguiente: 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>Recursos adicionales

- [DTBLEDIT](dtbledit.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

