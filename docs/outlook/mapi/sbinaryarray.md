---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438291"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de valores binarios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a>Miembros

 **cValues**
  
> Recuento de valores en la matriz a la que apunta el **miembro lpbin.** 
    
 **lpbin**
  
> Puntero a una matriz [de estructuras SBinary](sbinary.md) que contiene los valores binarios. 
    
## <a name="remarks"></a>Comentarios

La **estructura SBinaryArray** se usa para describir propiedades de tipo PT_MV_BINARY. 
  
Para obtener más información acerca PT_MV_BINARY, vea [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Consulte también



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

