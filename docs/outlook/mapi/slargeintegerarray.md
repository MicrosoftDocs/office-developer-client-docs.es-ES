---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382732"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de estructuras [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) que se utilizan para describir una propiedad de tipo PT_MV_I8. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Recuento de valores de la matriz indicada por el miembro **lpli** . 
    
 **lpli**
  
> Puntero a una matriz de estructuras **LARGE_INTEGER** manteniendo los valores enteros. 
    
## <a name="remarks"></a>Comentarios

Para obtener más información sobre PT_MV_18, vea la [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Vea también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

