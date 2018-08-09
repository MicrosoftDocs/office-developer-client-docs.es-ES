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
ms.openlocfilehash: 9734adff9c9c7526fc8ff46d17ca913752e104b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820595"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Hace referencia a**: Outlook 
  
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
  
## <a name="see-also"></a>Vea también



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

