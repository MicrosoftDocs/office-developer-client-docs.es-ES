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
ms.openlocfilehash: 553ec17e9caf9bf93278ff139eb94e02e6b48554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19820659"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**Hace referencia a**: Outlook 
  
Contiene una matriz de estructuras [GUID](guid.md) que se utilizan para describir una propiedad de tipo PT_MV_CLSID. 
  
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
  
> Recuento de valores de la matriz indicada por el miembro **lpguid** . 
    
 **lpguid**
  
> Puntero a una matriz de estructuras **GUID** que contiene los valores de identificador de clase. 
    
## <a name="remarks"></a>Comentarios

Para obtener más información sobre PT_MV_CLSID, vea la [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Vea también



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

