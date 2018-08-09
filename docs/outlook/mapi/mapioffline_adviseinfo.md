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
ms.openlocfilehash: 443644b66ba9c961992e22dbfc260fe8c48fe1b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818257"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Hace referencia a**: Outlook 
  
Proporciona información a **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** para registrar la devolución de llamada para un objeto sin conexión. 
  
## <a name="quick-info"></a>Información rápida

Vea **IMAPIOfflineMgr::Advise**. 
  
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
    
_ulClientToken_: un símbolo (token) definido por el cliente sobre una devolución de llamada. Es el miembro *ulClientToken* de la estructura **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** pasado a **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**. 
    
_CallbackType_: tipo de devolución de llamada para realizar.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - El tipo de devolución de llamada es por notificación. Esto es el único tipo admitido de devolución de llamada.  *pCallback* debe indicar la interfaz **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_pCallback_: interfaz que se usará para la devolución de llamada. Esto es la implementación del cliente de **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_ulAdviseTypes_: los tipos de advise, identificado por la condición para que advierte. El único tipo admitido es MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_ulStateMask_: el estado compatible sólo es MAPIOFFLINE_STATE_ALL.
    
## <a name="see-also"></a>Vea también

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [Información sobre la API de estado sin conexión](about-the-offline-state-api.md) 
- [Constantes MAPI](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)

