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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395941"
---
# <a name="ipersistmessageload"></a>IPersistMessage::Load

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Carga el formulario para un mensaje especificado.
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a>Parámetros

 _pMessageSite_
  
> [entrada] Un puntero al sitio de mensaje del formulario al que se va a cargar.
    
 _pMessage_
  
> [entrada] Un puntero al mensaje para el que se debe cargar el formulario.
    
 _ulMessageStatus_
  
> [entrada] Una máscara de bits de indicadores definidas por el cliente o definidas por el proveedor, copiada desde la propiedad del mensaje **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)), que proporcionan información sobre el estado del mensaje.
    
 _ulMessageFlags_
  
> [entrada] Una máscara de bits de indicadores, que se copió desde la propiedad del mensaje **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)), que proporcionar más información sobre el estado del mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario se cargó correctamente.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IPersistMessage::Load** para cargar un formulario para un mensaje existente. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

 **Carga** sólo se llama cuando un formulario está en uno de los siguientes estados: 
  
- [No inicializado](uninitialized-state.md)
    
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Si un visor de formulario llama **carga** mientras el formulario está en cualquier otro estado, el método devuelve E_UNEXPECTED. 
  
Si el formulario tiene una referencia a un sitio de mensaje activo distinto del que se pasó a la **carga**, la versión del sitio original debido a que ya no se usará. Almacenar los punteros para el sitio de mensaje y el mensaje de los parámetros _pMessageSite_ y _pMessage_ y llamar a métodos de [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) de ambos objetos para incrementar sus recuentos de referencia. 
  
Una vez haya finalizado **AddRef** , almacenar las propiedades de los parámetros _ulMessageStatus_ y _ulMessageFlags_ en el formulario. Realizar la transición del formulario a su estado [Normal](normal-state.md) antes de mostrarla y notificar a los visores registrados llamando a sus métodos [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) . 
  
Si no se producen errores, devuelve S_OK. 
  
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

