---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 01ea05eb864c78f3ded39ca3ebc62578076b9d37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584663"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela la responsabilidad de envío de notificaciones que se estableció previamente con una llamada al método [IMAPISupport::Subscribe](imapisupport-subscribe.md) . 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Parámetros

 _ulConnection_
  
> [entrada] El número de conexión distinto de cero que representa el registro de la notificación previamente establecido mediante **IMAPISupport::Subscribe**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha cancelado el registro de la notificación.
    
MAPI_E_NOT_FOUND 
  
> El número de conexión que se pasa en el parámetro _ulConnection_ no existe. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::Unsubscribe** se implementa para todos los objetos de soporte técnico de proveedor de servicio. Proveedores de servicios de llamada **Cancelar** para cancelar un registro configurado previamente por **suscribirse**a las notificaciones. **Cancelar** cancela el registro por liberar el puntero del receptor de advise pasado en la llamada **Subscribe** . 
  
Por lo general, se llama al método de **IUnknown:: Release** del receptor de notificaciones durante la llamada de **cancelación de suscripción** . Sin embargo, si otro subproceso está en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto de receptor advise, la llamada de la **versión** se retrasa hasta que el método **OnNotify** devuelve. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

