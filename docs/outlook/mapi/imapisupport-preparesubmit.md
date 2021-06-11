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
ms.openlocfilehash: 738eb346ec5388cbd94b32598236ef2ca05740f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425739"
---
# <a name="imapisupportpreparesubmit"></a>IMAPISupport::PrepareSubmit

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Prepara un mensaje para el envío a la cola MAPI.
  
```cpp
HRESULT PrepareSubmit(
LPMESSAGE lpMessage,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in] Puntero al mensaje que se debe preparar.
    
 _lpulFlags_
  
> [in, out] En la entrada, el  _parámetro lpulFlags_ está reservado y debe ser cero. Al salir,  _lpulFlags_ debe ser NULL. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje se preparó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::P repareSubmit** se implementa para objetos de soporte técnico del proveedor del almacén de mensajes. Los proveedores de almacén de mensajes llaman a **PrepareSubmit** en su implementación del método [IMessage::SubmitMessage](imessage-submitmessage.md) para preparar un mensaje para el envío a la cola MAPI. 
  
 **PrepareSubmit** se usa para controlar los mensajes que tienen la marca MSGFLAG_RESEND establecida en su **propiedad PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). MSGFLAG_RESEND se establece para los mensajes que incluyen una solicitud que se va a resentir cuando se produce un error en una transmisión inicial. **PrepareSubmit** determina cuál de los destinatarios de la lista de destinatarios recibió correctamente el mensaje y cuál no. 
  
Para obtener acceso a la lista de destinatarios, **PrepareSubmit** llama al método [IMessage::GetRecipientTable del](imessage-getrecipienttable.md) mensaje. Para recuperar los datos del destinatario, **PrepareSubmit** llama al método [IMAPITable::QueryRows](imapitable-queryrows.md) de la tabla de destinatarios. Para cada fila de la tabla, **PrepareSubmit** comprueba la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) y realiza una de las siguientes acciones:
  
- Si se MAPI_SUBMITTED marca, **PrepareSubmit** borra la marca y establece la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) en FALSE.
    
- Si la MAPI_SUBMITTED no está establecida, **PrepareSubmit** cambia PR_RECIPIENT_TYPE a MAPI_P1 y establece  **PR_RESPONSIBILITY** en TRUE. 
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Antes de llamar a **PrepareSubmit,** asegúrese de haber llamado al método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) y establecer la marca NOTIFY_READYTOSEND en el _parámetro ulFlags._ La **llamada SpoolerNotify** debe realizarse una vez por sesión antes de la llamada a **PrepareSubmit**. **SpoolerNotify** sincroniza la cola MAPI y garantiza que todos los proveedores de transporte necesarios hayan iniciado sesión y que sus tipos de direcciones estén registrados. 
  
## <a name="see-also"></a>Vea también



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

