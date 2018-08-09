---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e237e73f59fa691821dcb55b59f5d17518451797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817854"
---
# <a name="ipersistmessageinitnew"></a>IPersistMessage::InitNew

  
  
**Hace referencia a**: Outlook 
  
Inicializa un nuevo mensaje.
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parámetros

 _pMessageSite_
  
> [entrada] Un puntero al sitio de mensaje que el formulario se va a usar para trabajar con el mensaje en el Visor.
    
 _pMessage_
  
> [entrada] Un puntero al mensaje nuevo.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El nuevo mensaje se inicializó correctamente.
    
## <a name="remarks"></a>Comentarios

Visores de formulario, llame al método **IPersistMessage::InitNew** cuando el usuario escribe un mensaje nuevo que pertenece a una clase de mensaje que controla el formulario. Si el objeto de formulario tiene un puntero de interfaz de usuario válido, se debe mostrar la interfaz de usuario para el objeto de mensaje. 
  
 No se debe llamar **InitNew** cuando el formulario está en cualquier estado excepto el estado [Uninitialized](uninitialized-state.md) . Si el formulario está en uno de los demás Estados cuando se llama a **InitNew** , devolver E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Normalmente, los mensajes que han guardado los propiedades están marcados como modificado para que el cliente puede mostrar un cuadro de diálogo que solicita al usuario si se deben guardar estas propiedades. Si el usuario indica que se debe guardar un mensaje, guarde los datos, marcar el mensaje como limpio y salir normalmente.
  
Sin embargo, si el procesamiento para los mensajes recién inicializados incluye la configuración de uno o más propiedades calculan y es importante para las propiedades que se guarde, marcar los mensajes como modificado. Debido a que calcula las propiedades deben ser visibles para los usuarios, no se debe mostrar ningún cuadro de diálogo.
  
Si el formulario tiene una referencia a un sitio de mensaje activo distinto del que se pasó a **InitNew**, suelte el sitio original debido a que ya no se usará. Almacenar los punteros para el sitio de mensaje y el mensaje de los parámetros _pMessageSite_ y _pMessage_ y llamar a métodos de [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) de ambos objetos para incrementar sus recuentos de referencia. 
  
Establecer las propiedades de **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) para el nuevo mensaje y **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) a algo apropiado para su clase de mensaje. Muchas clases de mensaje, por ejemplo, establezca **PR_MESSAGE_FLAGS** en MSGFLAG_UNSENT para los mensajes nuevos. 
  
Antes de devolver, el formulario en el estado [Normal](normal-state.md) si no hay errores de transición se han producido. Enviar una notificación de mensaje nuevo a todos los visores registrados llamando a sus métodos [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) y devolver S_OK. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Después de realizar una llamada satisfactoria a **InitNew**, se puede asumir que se han establecido las siguientes propiedades necesarias y no otros, para el formulario:
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
Para obtener más información acerca de los Estados de los formularios, vea [Estados de formulario](form-states.md). Para obtener más información acerca de cómo se inicializan los objetos de almacenamiento, vea el método [IPersistStorage::InitNew](http://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Vea también



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

