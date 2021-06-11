---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430234"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cancela el envío de notificaciones configuradas anteriormente con una llamada al [método IMAPITable::Advise.](imapitable-advise.md) 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in] El número de la conexión de registro devuelta por una llamada a [IMAPITable::Advise](imapitable-advise.md).
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada ha sido correcta.
    
## <a name="remarks"></a>Comentarios

Use el método **IMAPITable::Unadvise** para liberar el puntero al objeto receptor advise pasado en el parámetro  _lpAdviseSink_ en la llamada anterior a **IMAPITable::Advise**, cancelando así un registro de notificación. Como parte de descartar el puntero al objeto receptor advise, se llama al método **IUnknown::Release** del objeto. Por lo general, **se** llama a Release durante la llamada **Unadvise,** pero si otro subproceso está en el proceso de llamar al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para el receptor de avisos, la llamada **Release** se retrasa hasta que el método **OnNotify** devuelve. 
  
Para obtener más información sobre el proceso de notificación, vea [Event Notification in MAPI](event-notification-in-mapi.md). Para obtener información específica acerca de la notificación de tabla, vea [About Table Notifications](about-table-notifications.md). Para obtener información acerca del uso de los **métodos IMAPISupport** para admitir notificaciones, vea [Supporting Event Notification](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI usa el **método IMAPITable::Unadvise** para cancelar las notificaciones de la tabla.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

