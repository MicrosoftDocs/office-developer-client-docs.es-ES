---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c207b1db6a24cc60967735e2f4b1a4aa97007750
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820697"
---
# <a name="slongarray"></a>SLongArray

  
  
**Se aplica a**: Outlook 
  
Contiene una matriz de tipos de valor de tipo LONG que se utilizan para describir una propiedad de tipo PT_MV_LONG. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>Miembros

 **cValues**
  
> Recuento de valores de la matriz indicada por el miembro **lpl** . 
    
 **lpl**
  
> Puntero a una matriz de valores de tipo LONG.
    
## <a name="remarks"></a>Notas

Para obtener más información sobre PT_MV_LONG, vea la [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Ver también



[SPropValue](spropvalue.md)


[Estructuras MAPI](mapi-structures.md)

