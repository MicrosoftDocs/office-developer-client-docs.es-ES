---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 9d8eb3f2c52f20ffe57d84823a0ed736337b4d9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818270"
---
# <a name="mapiofflinenotify"></a>MAPIOFFLINE_NOTIFY

**Se aplica a**: Outlook 
  
Se trata de la notificación de un cambio en el estado de conexión. Indica la parte del estado de conexión que ha cambiado, el estado de conexión anterior y el nuevo estado de conexión.
  
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

## <a name="members"></a>Miembros

 _ulSize_
  
> Tamaño de la estructura **MAPIOFFLINE_NOTIFY** . 
    
 _NotifyType_
  
> Tipo de notificación. Tenga en cuenta que se admite solo notificación sobre el cambio del estado de conexión; los únicos valores admitidos son:
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Un símbolo (token) definido por el cliente en la estructura **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** en **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
    
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
    
## <a name="remarks"></a>Notas

La API de estado sin conexión admite solamente las notificaciones de cambios en línea o sin conexión. Un cliente debe comprobar que Outlook devuelve los siguientes valores antes de examinar el cambio real:
  
1.  *NotifyType* tiene el valor MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE o MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. En este caso, el cliente puede asumir que el cambio es un cambio de estado de conexión, y es *información* de la estructura *StateChange* . 
    
2.  *ulMask* tiene el valor MAPIOFFLINE_STATE_OFFLINE_MASK. En este caso, el cliente puede asumir que el cambio es un cambio de estado de conexión o sin conexión y puede continuar con el examen de *ulStateOld* y *ulStateNew* . 
    
Es posible que Outlook notifica a un cliente de otros cambios que no son compatibles. En esos casos, *NotifyType* no sería uno de los tres valores que se ha indicado anteriormente, o *ulMask* no sería MAPIOFFLINE_STATE_OFFLINE_MASK y el cliente debe omitir el resto de los datos en *información* . 
  
## <a name="see-also"></a>Ver también

- [Acerca de la API de estado sin conexión](about-the-offline-state-api.md)  
- [Constantes MAPI](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)

