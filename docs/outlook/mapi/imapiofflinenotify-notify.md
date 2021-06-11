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
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410696"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Envía notificaciones al cliente sobre los cambios en el estado de conexión.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Parameters

 _pNotifyInfo_
  
> [in] La notificación que Outlook envía al cliente. La notificación indica la parte del estado de conexión que ha cambiado, el estado de conexión anterior y el nuevo estado de conexión.
    
## <a name="remarks"></a>Comentarios

Outlook este método para enviar devoluciones de llamada de notificación a un cliente. Para que esta interfaz esté disponible para Microsoft Outlook 2010 o Microsoft Outlook 2013, el cliente debe implementar esta interfaz y pasarle un puntero como miembro en **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** al configurar devoluciones de llamada con **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
  
El cliente también pasa **a MAPIOFFLINE_ADVISEINFO** un token de cliente que Outlook 2010 o Outlook 2013 usa en **IMAPIOfflineNotify::Notify** para identificar el cliente registrado para la devolución de llamada de notificación. 
  
En general, Outlook 2010 y Outlook 2013 pueden notificar a un cliente los cambios en línea/sin conexión y otros cambios de estado de conexión, pero la API de estado sin conexión solo admite notificaciones para cambios en línea o sin conexión. El cliente debe omitir todas las demás notificaciones.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de estado sin conexión](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

