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
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331699"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de valores de tiempo.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Número de valores de la matriz a los que señala el miembro **lpat** . 
    
 **lpat**
  
> Puntero a una matriz de valores de tiempo de aplicación. 
    
## <a name="remarks"></a>Comentarios

La estructura **SAppTimeArray** se usa para definir propiedades de tipo PT_MV_APPTIME. Para obtener más información acerca de PT_MV_APPTIME, vea [lista de tipos de propiedades](property-types.md).
  
## <a name="see-also"></a>Vea también



[Estructuras MAPI](mapi-structures.md)

