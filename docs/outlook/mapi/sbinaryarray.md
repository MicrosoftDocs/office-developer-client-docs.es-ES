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
ms.openlocfilehash: fd9a8d731d141dbb71a204a2d20b268951bef42f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820556"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**Hace referencia a**: Outlook 
  
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

## <a name="members"></a>Members

 **cValues**
  
> Recuento de valores de la matriz indicada por el miembro **lpbin** . 
    
 **lpbin**
  
> Puntero a una matriz de estructuras [SBinary](sbinary.md) que contiene los valores binarios. 
    
## <a name="remarks"></a>Comentarios

La estructura **SBinaryArray** se usa para describir las propiedades de tipo PT_MV_BINARY. 
  
Para obtener más información sobre PT_MV_BINARY, vea la [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Vea también



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

