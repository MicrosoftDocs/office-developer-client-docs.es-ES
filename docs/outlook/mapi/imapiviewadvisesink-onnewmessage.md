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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: adf9b28e941e9ead9b83660f58701f13f35cabc7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817628"
---
# <a name="imapiviewadvisesinkonnewmessage"></a>IMAPIViewAdviseSink::OnNewMessage

  
  
**Se aplica a**: Outlook 
  
Se notifica al Visor de formulario que ha cargado un nuevo o un mensaje existente en un formulario.
  
```cpp
HRESULT OnNewMessage( void );
```

## <a name="parameters"></a>Parámetros

None
  
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La notificación se ha realizado correctamente.
    
## <a name="remarks"></a>Notas

Objetos de formulario llaman al método de **IMAPIViewAdviseSink::OnNewMessage** siempre que se carga un mensaje en un formulario mediante los métodos [IPersistMessage::InitNew](ipersistmessage-initnew.md) o [IPersistMessage::Load](ipersistmessage-load.md) . 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Liberar su puntero al objeto form activo debido a que ya no apunta al mensaje que anteriormente estaba viendo el Visor. 
  
Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Ver también



[IMAPIForm: IUnknown](imapiformiunknown.md)
  
[IPersistMessage::InitNew](ipersistmessage-initnew.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)

