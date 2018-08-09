---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 24e16aeb1bbee1c35cf8fbd5813fb3e83b762187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818258"
---
# <a name="mapiofflineaggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**Hace referencia a**: Outlook 
  
La estructura se utiliza con [HrCreateOfflineObj](hrcreateofflineobj.md). 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a>Members

 **ulSize**
  
> El tamaño de la estructura.
    
 **pOuterObj**
  
> Un puntero al objeto IUnknown en el que se vaya a agregar este objeto. Esto permite que las llamadas QueryInterface pase al objeto creado.
    
 **pRefTrackRoot**
  
> Debe ser NULL.
    
## <a name="see-also"></a>Vea también



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

