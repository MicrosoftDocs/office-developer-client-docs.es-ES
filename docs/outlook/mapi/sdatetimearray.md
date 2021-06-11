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
ms.openlocfilehash: 9d9fd04776742383f40c6989bcf588b24b33d84b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406783"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de valores de tiempo que se usan para describir una propiedad de tipo PT_MV_SYSTIME.
  
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
  
> Recuento de valores de la matriz a la que apunta el **miembro lpft.** 
    
 **lpft**
  
> Puntero a una matriz de [estructuras FILETIME](filetime.md) que contienen los valores de hora. 
    
## <a name="remarks"></a>Comentarios

Para obtener más información sobre PT_MV_SYSTIME, [vea Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Vea también



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

