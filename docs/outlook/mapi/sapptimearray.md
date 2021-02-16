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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430388"
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

## <a name="members"></a>Miembros

 **cValues**
  
> Recuento de valores en la matriz a la que apunta el **miembro lpat.** 
    
 **lpat**
  
> Puntero a una matriz de valores de hora de la aplicación. 
    
## <a name="remarks"></a>Comentarios

La **estructura SAppTimeArray** se usa para definir propiedades de tipo PT_MV_APPTIME. Para obtener más información acerca PT_MV_APPTIME, vea [Lista de tipos de propiedad](property-types.md).
  
## <a name="see-also"></a>Consulte también



[Estructuras MAPI](mapi-structures.md)

