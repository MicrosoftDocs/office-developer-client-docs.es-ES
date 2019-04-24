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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339798"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de valores de tiempo que se usan para describir una propiedad de tipo PT_MV_SYSTIME.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Número de valores de la matriz a los que señala el miembro **LPFT** . 
    
 **LPFT**
  
> Puntero a una matriz de estructuras [FILETIME](filetime.md) que contiene los valores de tiempo. 
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca de PT_MV_SYSTIME, vea [lista de tipos de propiedades](property-types.md).
  
## <a name="see-also"></a>Vea también



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

