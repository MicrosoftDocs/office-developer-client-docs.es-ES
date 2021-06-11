---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6c5480a8f5e008c01c7ab8141317f5f19547ab10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414770"
---
# <a name="mapioffline_notify"></a>MAPIOFFLINE_NOTIFY

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta es la notificación de un cambio en el estado de conexión. Indica la parte del estado de conexión que ha cambiado, el estado de conexión anterior y el nuevo estado de conexión.
  
## <a name="quick-info"></a>Información rápida

Vea **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a>Members

 _ulSize_
  
> Tamaño de la **MAPIOFFLINE_NOTIFY** estructura. 
    
 _NotifyType_
  
> Tipo de notificación. Tenga en cuenta que solo se admite la notificación al cambiar el estado de conexión; los únicos valores admitidos son:
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Token definido por el cliente en la **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** de **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
    
 _ulMask_
  
> La parte del estado de conexión que ha cambiado. El único valor admitido es MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulStateOld_
  
> El estado de conexión anterior. Los únicos valores admitidos son:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> El nuevo estado de conexión. Los únicos valores admitidos son:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>Comentarios

La API de estado sin conexión solo admite notificaciones para cambios en línea o sin conexión. Un cliente debe comprobar que Outlook devuelve los siguientes valores antes de examinar el cambio real:
  
1.  *NotifyType*  tiene el valor MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE o MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. En este caso, el cliente puede asumir que el cambio es un cambio de estado de conexión y  *que Info*  es de la estructura  *StateChange*  . 
    
2.  *ulMask tiene*  el valor MAPIOFFLINE_STATE_OFFLINE_MASK. En este caso, el cliente puede asumir que el cambio es un cambio de estado de conexión en línea/sin conexión y puede continuar con el examen  *de ulStateOld*  y  *ulStateNew*  . 
    
Es posible que Outlook informe a un cliente de otros cambios que no son compatibles. En tales casos,  *NotifyType*  no sería ninguno de los tres valores indicados anteriormente, o  *ulMask*  no sería MAPIOFFLINE_STATE_OFFLINE_MASK, y el cliente debe omitir el resto de los datos en  *Info*  . 
  
## <a name="see-also"></a>Vea también

- [Información sobre la API de estado sin conexión](about-the-offline-state-api.md)  
- [Constantes MAPI](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

