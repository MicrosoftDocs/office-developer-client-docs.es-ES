---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6986ed7c9ab9932c5d95fcfb7f74f80088f21971
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580372"
---
# <a name="sdoublearray"></a>SDoubleArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de tipo Double que se usa para describir una propiedad de tipo PT_MV_DOUBLE.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Recuento de valores de la matriz indicada por el miembro **lpdbl** . 
    
 **lpdbl**
  
> Puntero a una matriz de valores de tipo double.
    
## <a name="remarks"></a>Comentarios

Para obtener más información sobre PT_MV_DOUBLE, vea la [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Recursos adicionales



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

