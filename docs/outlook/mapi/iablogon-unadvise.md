---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424080"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela las notificaciones configuradas anteriormente con una llamada al método [IABLogon::Advise.](iablogon-advise.md) 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parámetros

 _ulConnection_
  
> [entrada] El número de conexión asociado a un registro de notificación activo. Una llamada anterior a **Advise** debe haber devuelto el valor  _de ulConnection_.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificación se canceló correctamente.
    
## <a name="remarks"></a>Comentarios

MAPI llama al **método Unadvise** para cancelar un registro de notificación para un contenedor, un usuario de mensajería o un objeto de lista de distribución. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La implementación de **Unadvise** dependerá de si admite la notificación con la ayuda de MAPI o manualmente. Si MAPI proporciona soporte técnico, llame al [método IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) para cancelar el registro. Si hay otro subproceso en proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del receptor de avisos, se puede retrasar hasta que **OnNotify** haya devuelto. 
  
Para obtener más información acerca del proceso de notificación, vea [Notificación de eventos en MAPI.](event-notification-in-mapi.md) Para obtener información sobre cómo usar los [métodos IMAPISupport : IUnknown](imapisupportiunknown.md) para admitir notificaciones, vea [Notificación de eventos auxiliares.](supporting-event-notification.md)
  
## <a name="see-also"></a>Consulte también



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

