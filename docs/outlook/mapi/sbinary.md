---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f54ef96443e5c9fc5fb587f5a9c25388c1ff9cdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577425"
---
# <a name="sbinary"></a>SBinary

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una propiedad de tipo PT_BINARY.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a>Members

 **cb**
  
> Recuento de bytes en el miembro **lpb** . 
    
 **lpb**
  
> Puntero para el valor de la propiedad PT_BINARY.
    
## <a name="remarks"></a>Comentarios

Para obtener información acerca de los tipos de propiedad, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Recursos adicionales



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

