---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3cb110fdcbbd88e494c44ba2ed73cc26674638ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420027"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona información a **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** para registrar la devolución de llamada para un objeto sin conexión. 
  
## <a name="quick-info"></a>Información rápida

Vea **IMAPIOfflineMgr:: Advise**. 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a>Members

_ulSize_: el tamaño de **MAPIOFFLINE_ADVISEINFO**. 
    
_ulClientToken_: un token definido por el cliente sobre una devolución de llamada. Es el miembro *ulClientToken* de la estructura **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** que se pasa a **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)**. 
    
_CallbackType_: tipo de devolución de llamada que se va a realizar.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - El tipo de devolución de llamada es por notificación. Este es el único tipo de devolución de llamada admitido.  *pCallback* debe indicar la interfaz **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_pCallback_: interfaz que se va a usar para la devolución de llamada. Esta es la implementación del cliente de **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_ulAdviseTypes_: los tipos de Advise, identificados por la condición de aconsejar. El único tipo admitido es MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_ulStateMask_: el único estado admitido es MAPIOFFLINE_STATE_ALL.
    
## <a name="see-also"></a>Ver también

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [Información sobre la API de estado sin conexión](about-the-offline-state-api.md) 
- [Constantes MAPI](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

