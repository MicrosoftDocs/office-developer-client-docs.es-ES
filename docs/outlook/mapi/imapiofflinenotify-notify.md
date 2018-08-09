---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 54843339c6843e075ec769da5751ae2fe753f302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817398"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**Hace referencia a**: Outlook 
  
Envía notificaciones al cliente acerca de los cambios en el estado de conexión.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Parámetros

 _pNotifyInfo_
  
> [entrada] La notificación de que Outlook envíe al cliente. La notificación indica la parte del estado de conexión que ha cambiado, el estado de conexión anterior y el nuevo estado de conexión.
    
## <a name="remarks"></a>Comentarios

Outlook utiliza este método para enviar las devoluciones de llamada de notificación a un cliente. Para realizar esta interfaz disponible en Microsoft Outlook 2010 o Microsoft Outlook 2013, el cliente debe implementar esta interfaz y pasar un puntero a él como un miembro en **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** al configurar las devoluciones de llamada con **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**. 
  
El cliente también pasa al **MAPIOFFLINE_ADVISEINFO** un símbolo (token) de cliente que Outlook 2010 o 2013 de Outlook se usa en **IMAPIOfflineNotify::Notify** para identificar el cliente registrado para la devolución de llamada de notificación. 
  
En general, Outlook 2010 y Outlook 2013 pueden notificar a un cliente de cambios en línea o sin conexión y otros cambios de estado de conexión, pero la API de estado sin conexión admite solamente las notificaciones de cambios en línea o sin conexión. El cliente debe omitir todas las notificaciones de otras.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de estado sin conexión](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

