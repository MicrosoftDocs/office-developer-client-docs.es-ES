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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348884"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela las notificaciones que se configuraron anteriormente con una llamada al método [IABLogon:: Advise](iablogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> a El número de conexión asociado con un registro de notificación activo. Una llamada anterior a **Advise** debe haber devuelto el valor de _ulConnection_.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El registro de notificaciones se canceló correctamente.
    
## <a name="remarks"></a>Comentarios

MAPI llama al **** método unaconsejable para cancelar un registro de notificaciones para un contenedor, un usuario de mensajería o un objeto de lista de distribución. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

La implementación de **Unadvise** dependerá de si se admite la notificación con la ayuda de MAPI o manualmente. Si MAPI proporciona soporte técnico, llame al método [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md) para cancelar el registro. Si hay otro subproceso en proceso de llamar al método [IMAPIAdviseSink:: NotifyTo](imapiadvisesink-onnotify.md) del receptor de notificación, se puede retrasar hasta que se devuelva la **notificación** . 
  
Para obtener más información sobre el proceso de notificación, vea [notificación de eventos en MAPI](event-notification-in-mapi.md). Para obtener información acerca de cómo usar los métodos [IMAPISupport: IUnknown](imapisupportiunknown.md) para admitir notificaciones, consulte [admitir notificaciones de eventos](supporting-event-notification.md).
  
## <a name="see-also"></a>Vea también



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

