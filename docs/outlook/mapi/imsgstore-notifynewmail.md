---
title: IMsgStoreNotifyNewMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.NotifyNewMail
api_type:
- COM
ms.assetid: d0d003b0-f12f-4422-b71f-26886169461f
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: bdda950cd1fab66db46590e0b9141bb3d2a75221
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817755"
---
# <a name="imsgstorenotifynewmail"></a>IMsgStore::NotifyNewMail

  
  
**Hace referencia a**: Outlook 
  
Informa el almac�n de mensajes que ha llegado un mensaje nuevo. Se llama a este m�todo s�lo por la cola MAPI.
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>Par�metros

 _lpNotification_
  
> [entrada] Un puntero a una estructura de [notificaci�n](notification.md) que describa la notificaci�n de mensaje nuevo. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El almac�n de mensajes notific� correctamente.
    
## <a name="remarks"></a>Comentarios

Se llama al m�todo de **IMsgStore::NotifyNewMail** por la cola MAPI para notificar el almac�n de mensajes que est� listo para la entrega de un mensaje. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Cuando se llama a **NotifyNewMail**, env�e una notificaci�n de correo nuevo a todos los clientes registrados. Puede enviar la notificaci�n mediante una llamada a [IMAPISupport::Notify](imapisupport-notify.md), si opta por utilizar los m�todos del objeto de soporte t�cnico, o mediante su propia implementaci�n. Un cliente registrado es uno que se llama [IMsgStore::Advise](imsgstore-advise.md) y se establece el par�metro  _lpEntryID_ en NULL y el par�metro  _ulEventMask_ a  _fnevNewMail_. 
  
No puede modificar ni liberar la memoria para la estructura de [notificaci�n](notification.md) que describe la notificaci�n de correo nuevo. Copie la estructura de **NOTIFICATION** mediante una llamada a la funci�n de utilidad [ScCopyNotifications](sccopynotifications.md) para hacer uso de la informaci�n de sus miembros. 
  
## <a name="see-also"></a>Vea tambi�n



[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
  
[Notificaci�n](notification.md)
  
[ScCopyNotifications](sccopynotifications.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

