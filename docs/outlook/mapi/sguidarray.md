---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3d20a0932de0fb29ea73e56c37e262c0ccd062c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424927"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de [estructuras GUID](guid.md) que se usan para describir una propiedad de tipo PT_MV_CLSID. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Recuento de valores en la matriz apuntada por el **miembro lpguid.** 
    
 **lpguid**
  
> Puntero a una matriz de **estructuras GUID** que contiene los valores de identificador de clase. 
    
## <a name="remarks"></a>Comentarios

Para obtener más información sobre PT_MV_CLSID, [vea List of Property Types](property-types.md).
  
## <a name="see-also"></a>Vea también



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

