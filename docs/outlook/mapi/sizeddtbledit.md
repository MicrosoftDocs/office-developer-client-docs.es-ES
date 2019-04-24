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
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282806"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea una estructura con nombre que incluye una estructura [DTBLEDIT](dtbledit.md) para describir un control de edición y el número máximo de caracteres que se pueden escribir en el control. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
|Estructura relacionada:  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Parameters

_n_
  
> Número máximo de caracteres que se pueden escribir en el control de edición.
    
_u_
  
> Nombre de la nueva estructura.
    
## <a name="remarks"></a>Comentarios

La macro **SizedDtblEdit** permite definir un control de edición cuando se conoce el número de caracteres habilitados. La nueva estructura se crea con los siguientes miembros: 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Para usar un puntero a la estructura resultante desde la macro **SizedDtblEdit** como un puntero de estructura **DTBLEDIT** , realice la siguiente conversión: 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>Vea también

- [DTBLEDIT](dtbledit.md)
- [Macros relacionadas con estructuras](macros-related-to-structures.md)

