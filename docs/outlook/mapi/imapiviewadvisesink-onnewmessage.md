---
title: IMAPIViewAdviseSinkOnNewMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnNewMessage
api_type:
- COM
ms.assetid: 0a2fb371-90ea-41dc-b2ab-051cf790e85a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6a6f8f9d675bee362b4a9f1c5b7fc544fa66d7b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419607"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Notifica al visor de formularios que se ha cargado un mensaje nuevo o existente en un formulario.
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>Parámetros

Ninguno
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha publicado correctamente.
    
## <a name="remarks"></a>Comentarios

Los objetos de formulario llaman al método **IMAPIViewAdviseSink::OnNewMessage** siempre que se carga un mensaje en un formulario mediante el método [IPersistMessage::InitNew](ipersistmessage-initnew.md) o [IPersistMessage::Load.](ipersistmessage-load.md) 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Libere el puntero activo al objeto de formulario porque ya no apunta al mensaje que el visor estaba viendo anteriormente. 
  
Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario.](sending-and-receiving-form-notifications.md)
  
## <a name="see-also"></a>Consulte también



[IMAPIForm : IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

