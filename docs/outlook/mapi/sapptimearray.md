---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d277908d3ec96537f63511e4d50488a694696bd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581226"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de valores de hora.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Recuento de valores de la matriz indicada por el miembro **lpat** . 
    
 **lpat**
  
> Puntero a una matriz de valores de tiempo de aplicación. 
    
## <a name="remarks"></a>Comentarios

La estructura **SAppTimeArray** se usa para definir las propiedades de tipo PT_MV_APPTIME. Para obtener más información sobre PT_MV_APPTIME, vea la [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Recursos adicionales



[Estructuras MAPI](mapi-structures.md)

