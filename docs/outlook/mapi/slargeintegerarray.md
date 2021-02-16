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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331391"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz [de LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) que se usan para describir una propiedad de tipo PT_MV_I8. 
  
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

## <a name="members"></a>Miembros

 **cValues**
  
> Recuento de valores en la matriz a la que apunta el **miembro lpli.** 
    
 **lpli**
  
> Puntero a una matriz de **LARGE_INTEGER** estructuras que mantienen los valores enteros. 
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca PT_MV_18, vea [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Consulte también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

