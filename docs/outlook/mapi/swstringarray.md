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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820815"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Se aplica a**: Outlook 
  
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

## <a name="members"></a>Miembros

 **cValues**
  
> Recuento de las cadenas en la matriz indicada por el miembro **lppszW** . 
    
 **lppszW**
  
> Puntero a una matriz de cadenas de caracteres Unicode terminado en null.
    
## <a name="remarks"></a>Notas

Para obtener más información sobre PT_MV_UNICODE, vea [Tipos de propiedades](property-types.md).
  
## <a name="see-also"></a>Ver también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

