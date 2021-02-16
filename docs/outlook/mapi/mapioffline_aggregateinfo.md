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
ms.openlocfilehash: 4775de0707eb90549f07525e3aa54ec5842f6050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438165"
---
# <a name="mapioffline_aggregateinfo"></a>MAPIOFFLINE_AGGREGATEINFO

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La estructura se usa con [HrCreateOfflineObj](hrcreateofflineobj.md). 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a>Miembros

 **ulSize**
  
> Tamaño de la estructura.
    
 **pOuterObj**
  
> Puntero al objeto IUnknown en el que se va a agregar este objeto. Esto permite que cualquier llamada QueryInterface pase al objeto creado.
    
 **pRefTrackRoot**
  
> Debe ser NULL.
    
## <a name="see-also"></a>Consulte también



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_CREATEINFO](mapioffline_createinfo.md)

