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
ms.openlocfilehash: f27da216b9c474aa31503917a6d3c7a74eab9c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421217"
---
# <a name="imapisupportunsubscribe"></a>IMAPISupport::Unsubscribe

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela la responsabilidad de enviar notificaciones establecidas anteriormente con una llamada al método [IMAPISupport::Subscribe.](imapisupport-subscribe.md) 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a>Parámetros

 _ulConnection_
  
> [entrada] El número de conexión distinto de cero que representa el registro de notificación previamente establecido a través de **IMAPISupport::Subscribe**.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se canceló el registro de notificación.
    
MAPI_E_NOT_FOUND 
  
> El número de conexión pasado en  _el parámetro ulConnection_ no existe. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::Unsubscribe** se implementa para todos los objetos de compatibilidad del proveedor de servicios. Los proveedores de servicios llaman a **Unsubscribe** para cancelar un registro de notificación previamente configurado por **Subscribe**. **Cancelar** la suscripción cancela el registro liberando el puntero del receptor de aviso pasado en la llamada **de suscripción.** 
  
Por lo general, se llama al método **IUnknown::Release** del receptor de avisos durante la llamada **de cancelación de** suscripción. Sin embargo, si hay otro subproceso en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el objeto receptor de aviso, la llamada **release** se retrasa hasta que el método **OnNotify** devuelve. 
  
## <a name="see-also"></a>Consulte también



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

