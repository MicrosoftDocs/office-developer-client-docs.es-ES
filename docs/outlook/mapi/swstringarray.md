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
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413608"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de cadenas de caracteres que se usan para describir una propiedad de tipo PT_MV_UNICODE. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Número de cadenas en la matriz a las que apunta el miembro **lppszW** . 
    
 **lppszW**
  
> Puntero a una matriz de cadenas de caracteres Unicode terminadas en NULL.
    
## <a name="remarks"></a>Comentarios

Para obtener más información acerca de PT_MV_UNICODE, vea [tipos de propiedades](property-types.md).
  
## <a name="see-also"></a>Ver también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

