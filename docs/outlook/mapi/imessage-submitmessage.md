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
ms.openlocfilehash: 1d325c67c836e727d8285bd2dceecf88bf68327c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817654"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**Hace referencia a**: Outlook 
  
Guarda todas las propiedades del mensaje y marca el mensaje como listo para ser enviado.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Máscara de bits de indicadores que se utilizan para controlar cómo se envía un mensaje. Se puede establecer la marca siguiente:
    
FORCE_SUBMIT 
  
> MAPI debe enviar el mensaje inmediatamente. Esta marca no está actualmente en uso.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NO_RECIPIENTS 
  
> Tabla de destinatarios del mensaje está vacía.
    
## <a name="remarks"></a>Comentarios

El método **IMessage::SubmitMessage** marca un mensaje como listo para ser transmitidos. MAPI pasa los mensajes al sistema de mensajería subyacente en el orden en que están marcados para el envío. Debido a esta funcionalidad, puede permanecer en un mensaje en un almacén de mensajes para algún tiempo antes de que el sistema de mensajería subyacente puede asumir la responsabilidad de él. El orden de recepción en el destino se encuentra en el control del sistema mensajería subyacente y no necesariamente deben coincidir con el orden en que se enviaron mensajes. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje para guardarlo y, a continuación, compruebe la propiedad del mensaje **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Si se establece la marca MSGFLAG_RESEND, llame a [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md). **PrepareSubmit** actualiza el tipo de destinatario y la propiedad de **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) para todos los destinatarios en el mensaje de reenvío.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se devuelve en **SubmitMessage** , todos los punteros en el mensaje y sus mensajes asociados subobjetos, carpetas, datos adjuntos, secuencias, tablas y así sucesivamente ya no son válidos. MAPI no permite las operaciones posteriores en estos punteros, salvo llamar a sus métodos **IUnknown:: Release** . MAPI está diseñada para que después de llamar a **SubmitMessage** , debe liberar el mensaje y todos sus subobjetos. Sin embargo, si **SubmitMessage** devuelve un valor de error que indica la información que falta o no es válido, el mensaje permanece abierto y los punteros siguen siendo válidos. 
  
Para cancelar una operación de envío, obtener y almacenar un puntero a la propiedad del mensaje de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) antes de que se envíe el mensaje. Debido a que el identificador de entrada de un mensaje se invalida después de que se ha enviado el mensaje, es necesario guardar antes de llamar a **SubmitMessage**. Para cancelar el envío, seleccione el parámetro _lpEntryId_ para este identificador de entrada y llame a [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI usa el método **IMessage::SubmitMessage** para enviar el mensaje seleccionado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

