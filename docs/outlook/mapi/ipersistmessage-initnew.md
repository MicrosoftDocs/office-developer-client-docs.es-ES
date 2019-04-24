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
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317153"
---
# <a name="ipersistmessageinitnew"></a>IPersistMessage::InitNew

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Inicializa un mensaje nuevo.
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parameters

 _pMessageSite_
  
> a Un puntero al sitio del mensaje que el formulario usará para trabajar con el mensaje en el visor.
    
 _pMessage_
  
> a Un puntero al nuevo mensaje.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El nuevo mensaje se inicializó correctamente.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IPersistMessage:: InitNew** cuando el usuario escribe un mensaje nuevo que pertenece a una clase de mensaje que el formulario administra. Si el objeto Form tiene un puntero de interfaz de usuario válido, se debe mostrar la interfaz de usuario del objeto Message. 
  
 No se debe llamar a **InitNew** cuando el formulario está en cualquier estado excepto el estado sin [inicializar](uninitialized-state.md) . Si el formulario está en uno de los demás Estados cuando se llama a **InitNew** , devuelva E_UNEXPECTED. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Normalmente, los mensajes que tienen propiedades no guardadas se marcan como modificados para que el cliente pueda mostrar un cuadro de diálogo en el que se pregunta al usuario si se deben guardar estas propiedades. Si el usuario indica que debe guardarse un mensaje, guardar los datos, marcar el mensaje como limpio y salir con normalidad.
  
Sin embargo, si el procesamiento de los mensajes recién inicializados incluye la configuración de una o más propiedades calculadas y es importante que se guarden las propiedades, no marque los mensajes como modificados. Como las propiedades calculadas deben ser invisibles para los usuarios, no debe mostrarse ningún cuadro de diálogo.
  
Si el formulario tiene una referencia a un sitio de mensajes activo distinto del que se pasa a **InitNew**, libere el sitio original porque ya no se usará. Almacene los punteros en el sitio y el mensaje de mensaje desde los parámetros _pMessageSite_ y _pMessage_ , y llame a los dos objetos [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) para incrementar sus recuentos de referencia. 
  
Establezca las propiedades **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) y **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del nuevo mensaje en algo apropiado para la clase de mensaje. Muchas clases de mensajes, por ejemplo, establecen **PR_MESSAGE_FLAGS** en MSGFLAG_UNSENT para los mensajes nuevos. 
  
Antes de devolverlo, pase el formulario al estado [normal](normal-state.md) si no se han producido errores. Envíe una notificación de mensaje nuevo a todos los visores registrados llamando a sus métodos [IMAPIViewAdviseSink:: OnNewMessage](imapiviewadvisesink-onnewmessage.md) y devuelva S_OK. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Después de realizar una llamada correcta a **InitNew**, puede suponer que se han establecido las siguientes propiedades obligatorias y ninguna otra para el formulario:
  
 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))
  
 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
  
 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))
  
 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
  
 **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))
  
 **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
  
 **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))
  
Para obtener más información acerca de los Estados de los formularios, consulte [Form States](form-states.md). Para obtener más información sobre cómo se inicializan los objetos de almacenamiento, vea el método [IPersistStorage:: InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Vea también



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

