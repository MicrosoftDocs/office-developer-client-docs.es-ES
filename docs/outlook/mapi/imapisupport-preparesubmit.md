---
title: IMAPISupportPrepareSubmit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.PrepareSubmit
api_type:
- COM
ms.assetid: 467242e3-96c9-4280-9cbc-9ecfe3f279cf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5f45a6457bba738b290d967260bbd34c0f88f93f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595065"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Prepara un mensaje para el envío a la cola de MAPI.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpMessage_
  
> [entrada] Un puntero al mensaje para preparar.
    
 _lpulFlags_
  
> [entrada, salida] En la entrada, el parámetro _lpulFlags_ está reservado y debe ser cero. En la salida, _lpulFlags_ debe ser NULL. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje se ha preparado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::PrepareSubmit** se implementa para objetos de soporte técnico de proveedor de almacén de mensajes. Los proveedores de almacén de mensajes llamada **PrepareSubmit** en su implementación del método [IMessage::SubmitMessage](imessage-submitmessage.md) para preparar un mensaje para el envío a la cola de MAPI. 
  
 **PrepareSubmit** se usa para administrar los mensajes que tienen la marca MSGFLAG_RESEND establecida en su propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). MSGFLAG_RESEND se establece para los mensajes que incluyen una solicitud para ser reenviados cuando se produce un error en una transmisión inicial. **PrepareSubmit** determina cuál de los destinatarios en la lista de destinatarios recibió correctamente el mensaje y que no lo ha hecho. 
  
Para obtener acceso a la lista de destinatarios, **PrepareSubmit** llama (método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) ) del mensaje. Para recuperar los datos de destinatario, **PrepareSubmit** llama a método [IMAPITable:: QueryRows](imapitable-queryrows.md) de destinatario de la tabla. Para cada fila de la tabla, **PrepareSubmit** comprueba la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) y toma una de las siguientes acciones:
  
- Si se establece la marca MAPI_SUBMITTED, **PrepareSubmit** borra la marca y la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) se establece en FALSE.
    
- Si no está establecido el indicador MAPI_SUBMITTED, **PrepareSubmit** cambia de **PR_RECIPIENT_TYPE** a MAPI_P1 y establece **PR_RESPONSIBILITY** en TRUE. 
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Antes de llamar a **PrepareSubmit**, asegúrese de que se ha llamado al método [SpoolerNotify](imapisupport-spoolernotify.md) y establece el indicador NOTIFY_READYTOSEND en el parámetro _ulFlags indicado_ . La llamada **SpoolerNotify** debe realizarse una vez por sesión antes de la llamada a **PrepareSubmit**. **SpoolerNotify** sincroniza a la cola MAPI y se asegura de que todos los proveedores de transporte necesarios se registran y sus tipos de dirección se registran. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

