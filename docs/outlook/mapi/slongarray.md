---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9b1c5a09a60240efa9d4fa117f0d8fe8113169d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361170"
---
# <a name="slongarray"></a>SLongArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de tipos de valor LONG que se usan para describir una propiedad de tipo PT_MV_LONG. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Número de valores de la matriz a los que señala el miembro **LPL** . 
    
 **LPL**
  
> Puntero a una matriz de valores de tipo LONG.
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca de PT_MV_LONG, vea [lista de tipos de propiedades](property-types.md).
  
## <a name="see-also"></a>Vea también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

