---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317132"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Carga el formulario para un mensaje especificado.
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a>Parameters

 _pMessageSite_
  
> a Un puntero al sitio del mensaje para el formulario que se va a cargar.
    
 _pMessage_
  
> a Un puntero al mensaje para el que se debe cargar el formulario.
    
 _ulMessageStatus_
  
> a Máscara de bits de marcas definidas por el cliente o definidas por el proveedor, copiadas de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje, que proporcionan información sobre el estado del mensaje.
    
 _ulMessageFlags_
  
> a Una máscara de datos de marcas, copiada de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje, que proporciona más información sobre el estado del mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario se cargó correctamente.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IPersistMessage:: Load** para cargar un formulario para un mensaje existente. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

 La **carga** sólo se llama cuando un formulario está en uno de los siguientes Estados: 
  
- [Sin inicializar](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Si un visor de formularios llama a **Load** mientras el formulario está en cualquier otro Estado, el método devuelve E_UNEXPECTED. 
  
Si el formulario tiene una referencia a un sitio de mensajes activo distinto del que se pasa a **Load**, libere el sitio original porque ya no se usará. Almacene los punteros en el sitio y el mensaje de mensaje desde los parámetros _pMessageSite_ y _pMessage_ , y llame a los dos objetos [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) para incrementar sus recuentos de referencia. 
  
Una vez finalizado **AddRef** , almacene las propiedades de los parámetros _ulMessageStatus_ y _ulMessageFlags_ en el formulario. Cambie el formulario a su estado [normal](normal-state.md) antes de mostrarlo y notifique a los visores registrados llamando a sus métodos [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) . 
  
Si no se produce ningún error, devuelva S_OK. 
  
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propiedad canónica PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estado sin inicializar](uninitialized-state.md)
  
[Estado HandsOffAfterSave](handsoffaftersave-state.md)
  
[Estado HandsOffFromNormal](handsofffromnormal-state.md)
  
[Estados de formulario](form-states.md)


[IPersistStorage:: Load](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[IPersistStream:: Load](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[IPersistFile:: Load](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

