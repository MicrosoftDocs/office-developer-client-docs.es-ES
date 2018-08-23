---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e3f53a894b7f7cdaa68e66530c7bd99bf49b9ed0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581359"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de cadenas de caracteres que se utilizan para describir una propiedad de tipo PT_MV_UNICODE. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Recuento de las cadenas en la matriz indicada por el miembro **lppszW** . 
    
 **lppszW**
  
> Puntero a una matriz de cadenas de caracteres Unicode terminado en null.
    
## <a name="remarks"></a>Comentarios

Para obtener más información sobre PT_MV_UNICODE, vea [Tipos de propiedades](property-types.md).
  
## <a name="see-also"></a>Recursos adicionales



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

