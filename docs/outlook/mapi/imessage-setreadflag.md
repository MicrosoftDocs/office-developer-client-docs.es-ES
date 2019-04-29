---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439873"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece o borra la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje y administra el envío de informes de lectura.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

_ulFlags_
  
> a Máscara de la máscara que controla la configuración de la marca de lectura de un mensaje es decir, la marca MSGFLAG_READ del mensaje en su propiedad **PR_MESSAGE_FLAGS** y el procesamiento de los informes de lectura. Se pueden establecer los siguientes indicadores: 
    
  - CLEAR_READ_FLAG: la marca MSGFLAG_READ debe borrarse en **PR_MESSAGE_FLAGS** y no debe enviarse ningún informe de lectura. 
      
  - CLEAR_NRN_PENDING: la marca MSGFLAG_NRN_PENDING se debe borrar en **PR_MESSAGE_FLAGS** y no se debe enviar un informe que no sea de lectura. 
      
  - CLEAR_RN_PENDING: la marca MSGFLAG_RN_PENDING debe borrarse en **PR_MESSAGE_FLAGS** y no debe enviarse ningún informe de lectura. 
      
  - GENERATE_RECEIPT_ONLY: se debe enviar un informe de lectura si hay uno pendiente, pero no debe haber ningún cambio en el estado de la marca MSGFLAG_READ.
      
  - MAPI_DEFERRED_ERRORS: permite que **SetReadFlag** se devuelva correctamente, posiblemente antes de que se haya completado la operación. 
      
  - SUPPRESS_RECEIPT: se debe cancelar un informe de lectura pendiente si se ha solicitado un informe de lectura y esta llamada cambia el estado del mensaje de no leído a leído. Si esta llamada no cambia el estado del mensaje, el proveedor del almacén de mensajes puede omitir esta marca.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La marca de lectura del mensaje se ha configurado o borrado correctamente.
    
MAPI_E_NO_SUPPRESS 
  
> El proveedor de almacenamiento de mensajes no admite la supresión de informes de lectura.
    
MAPI_E_INVALID_PARAMETER 
  
> Una de las siguientes combinaciones de marcas se establece en el parámetro _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Comentarios

El método **IMessage:: SetReadFlag** establece o borra la marca MSGFLAG_READ del mensaje en la propiedad **PR_MESSAGE_FLAGS** y llama a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para guardar el mensaje. Si se establece la marca MSGFLAG_READ, se marca un mensaje como leído, lo que no indica necesariamente que el destinatario previsto haya leído realmente el mensaje. 
  
**SetReadFlags** también administra el envío de informes de lectura. Se envía un informe de lectura solo si el remitente ha solicitado uno. 
  
No se puede modificar la marca de lectura para:
  
- Mensajes que no existen.
    
- Mensajes que se movieron en otro lugar.
    
- Mensajes que están abiertos con permiso de lectura y escritura.
    
- Mensajes que se envían actualmente.
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Si no se establece ninguno de los indicadores en el parámetro _ulFlags_ , se aplican las siguientes reglas: 
  
- Si MSGFLAG_READ ya está establecido, no haga nada.
    
- Si no se establece MSGFLAG_READ, establézcalo y envíe los informes de lectura pendientes si se establece la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).
    
Si se establecen las dos marcas SUPPRESS_RECEIPT y GENERATE_RECEIPT_ONLY, se debe borrar el bit PR_READ_RECEIPT_REQUESTED, si se establece, y no se debe enviar un informe de lectura.
  
Cuando se establece la marca SUPPRESS_RECEIPT:
  
- Si MSGFLAG_READ ya está establecido, no haga nada. 
    
- Si no se establece MSGFLAG_READ, establézcalo y cancele los informes de lectura pendientes.
    
Cuando se establece la marca CLEAR_READ_FLAG, borre la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** de cada mensaje y no envíe ningún informe de lectura. 
  
Cuando se establece la marca GENERATE_RECEIPT_ONLY, enviar los informes de lectura pendientes. No establezca ni borre MSGFLAG_READ.
  
Cuando se establecen las dos marcas SUPPRESS_RECEIPT y GENERATE_RECEIPT_ONLY, se establece la propiedad PR_READ_RECEIPT_REQUESTED en FALSE si se establece y no se envía un informe de lectura.
  
Puede optimizar el comportamiento del informe suprimiendo la generación de informes de lectura en determinadas condiciones. Sin embargo, si no admite la supresión de informes y un cliente llama a **SetReadFlag** con el conjunto de marcas SUPPRESS_RECEIPT, devuelve MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnSetReadFlag  <br/> |MFCMAPI usa el método **IMessage:: SetReadFlag** para establecer las marcas de lectura en los mensajes seleccionados.  <br/> |
   
## <a name="see-also"></a>Ver también

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

