---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dc90f15835de35354a271d87a736366a4caf8dd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578783"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de valores de hora que se utilizan para describir una propiedad de tipo PT_MV_SYSTIME.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Recuento de valores de la matriz indicada por el miembro **lpft** . 
    
 **lpft**
  
> Puntero a una matriz de estructuras [FILETIME](filetime.md) que contienen los valores de tiempo. 
    
## <a name="remarks"></a>Comentarios

Para obtener más información sobre PT_MV_SYSTIME, vea la [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Recursos adicionales



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

