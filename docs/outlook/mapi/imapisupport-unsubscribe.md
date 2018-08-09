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
ms.openlocfilehash: 9ee071bb303c7518a23c5e57909f8618b7aebdde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817564"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**Hace referencia a**: Outlook 
  
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
  
## <a name="see-also"></a>Vea también



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

