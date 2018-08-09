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
ms.openlocfilehash: 834a7141f0e7150140fa27c21d88db422d6f5561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820548"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**Hace referencia a**: Outlook 
  
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
  
## <a name="see-also"></a>Vea también



[Estructuras MAPI](mapi-structures.md)

