---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 64e5cf31dffdc794a22bcbd6d503a2b688f9c733
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332210"
---
# <a name="indexsearchpusherprocess"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el proceso que envía una notificación al controlador de protocolo MAPI que un objeto de ese almacén está preparado para la indización.
  
## <a name="quick-info"></a>Información rápida

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Miembros

 *dwPID* 
  
>  IDENTIFICADOR de proceso del proceso que envía una notificación de indización al indizador del controlador de protocolo MAPI. 
    

