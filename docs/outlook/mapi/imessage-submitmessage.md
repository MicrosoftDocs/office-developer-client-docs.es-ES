---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437367"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Guarda todas las propiedades del mensaje y marca el mensaje como listo para enviarse.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Máscara de bits de las marcas usadas para controlar cómo se envía un mensaje. Se puede establecer la siguiente marca:
    
FORCE_SUBMIT 
  
> MAPI debe enviar el mensaje inmediatamente. Esta marca no está actualmente en uso.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_RECIPIENTS 
  
> La tabla de destinatarios del mensaje está vacía.
    
## <a name="remarks"></a>Comentarios

El **método IMessage::SubmitMessage** marca un mensaje como listo para transmitirse. MAPI pasa mensajes al sistema de mensajería subyacente en el orden en que se marcan para el envío. Debido a esta funcionalidad, un mensaje puede permanecer en un almacén de mensajes durante algún tiempo antes de que el sistema de mensajería subyacente pueda asumir su responsabilidad. El orden de recepción en el destino está en el control del sistema de mensajería subyacente y no coincide necesariamente con el orden en que se enviaron los mensajes. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje para guardarlo y, a continuación, compruebe la propiedad PR_MESSAGE_FLAGS **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje. Si se MSGFLAG_RESEND marca, llame a [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md). **PrepareSubmit actualiza** el tipo de destinatario y **la PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para todos los destinatarios del mensaje de reenvío.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando **SubmitMessage** devuelve, todos los punteros al mensaje y sus subobjetos asociados mensajes, carpetas, datos adjuntos, secuencias, tablas, entre otros, ya no son válidos. MAPI no permite ninguna otra operación en estos punteros, excepto para llamar a sus **métodos IUnknown::Release.** MAPI está diseñado de forma que, después de llamar **a SubmitMessage,** debe liberar el mensaje y todos los subobjetos asociados. Sin embargo, **si SubmitMessage** devuelve un valor de error que indica que falta información o que no es válida, el mensaje permanece abierto y los punteros siguen siendo válidos. 
  
Para cancelar una operación de envío, obtenga y almacene un puntero a la propiedad PR_ENTRYID **del** mensaje ([PidTagEntryId](pidtagentryid-canonical-property.md)) antes de enviar el mensaje. Dado que el identificador de entrada de un mensaje se invalida después de enviar el mensaje, es necesario guardarlo antes de llamar a **SubmitMessage**. Para cancelar el envío, señale el parámetro  _lpEntryId_ a este identificador de entrada y llame a [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI usa el **método IMessage::SubmitMessage** para enviar el mensaje seleccionado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

