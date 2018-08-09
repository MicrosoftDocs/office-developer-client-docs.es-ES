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
ms.openlocfilehash: 0ae35166f01f597c2c3ab399a1b66e5760ab0dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817650"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**Hace referencia a**: Outlook 
  
Establece o borra el indicador MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje y administra el envío de informes de lectura.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

_ulFlags_
  
> [entrada] Máscara de bits de indicadores que controla la configuración de lectura de un mensaje, es decir, marca marca MSGFLAG_READ del mensaje en su propiedad **PR_MESSAGE_FLAGS** y el procesamiento de informes de lectura. Se pueden establecer los siguientes indicadores: 
    
  - CLEAR_READ_FLAG: Se debe borrar la marca MSGFLAG_READ en **PR_MESSAGE_FLAGS** y no se debe enviar ningún informe de lectura. 
      
  - CLEAR_NRN_PENDING: Se debe borrar la marca MSGFLAG_NRN_PENDING en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de no leído. 
      
  - CLEAR_RN_PENDING: Se debe borrar la marca MSGFLAG_RN_PENDING en **PR_MESSAGE_FLAGS** y no se debe enviar ningún informe de lectura. 
      
  - GENERATE_RECEIPT_ONLY: Se debe enviar un informe de lectura si uno está pendiente, pero no debe haber ningún cambio en el estado de la marca MSGFLAG_READ.
      
  - MAPI_DEFERRED_ERRORS: Permite **SetReadFlag** devolver de correctamente, posiblemente antes de que la operación ha finalizado. 
      
  - SUPPRESS_RECEIPT: Se debe cancelar un informe de lectura pendiente si se solicita un informe de lectura y esta llamada cambia el estado del mensaje de no leído a leer. Si esta llamada no cambia el estado del mensaje, el proveedor de almacenamiento de mensajes puede pasar por alto esta marca.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Indicador de lectura del mensaje se ha establecido correctamente o desactivada.
    
MAPI_E_NO_SUPPRESS 
  
> El proveedor de almacén de mensajes no es compatible con la supresión de informes de lectura.
    
MAPI_E_INVALID_PARAMETER 
  
> Una de las siguientes combinaciones de indicadores se establece en el parámetro _ulFlags indicado_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Comentarios

El método **IMessage::SetReadFlag** establece o borra la marca MSGFLAG_READ del mensaje en la propiedad **PR_MESSAGE_FLAGS** y llamadas [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para guardar el mensaje. Establecer el indicador MSGFLAG_READ marca un mensaje como lectura, que no necesariamente indica que el destinatario realmente ha leído el mensaje. 
  
**SetReadFlags** también administra el envío de informes de lectura. Se envía un informe de lectura sólo si el remitente ha solicitado una. 
  
No se puede modificar la marca de lectura para:
  
- Mensajes que no existen.
    
- Los mensajes que se han moverán a otro lugar.
    
- Mensajes que están abiertos con permiso de lectura y escritura.
    
- Mensajes que se envían actualmente.
    
## <a name="notes-to-callers"></a>Notas para los llamadores

Si ninguno de los indicadores se establecen en el parámetro _ulFlags_ , se aplican las siguientes reglas: 
  
- Si MSGFLAG_READ ya está establecido, no haga nada.
    
- Si no se establece MSGFLAG_READ, configurarla y enviarlas pendientes informes de lectura si se establece la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).
    
Si se establecen las marcas de la SUPPRESS_RECEIPT y la GENERATE_RECEIPT_ONLY, la PR_READ_RECEIPT_REQUESTED de MAPI bit, si se establece, se deben borrar y no se debe enviar un informe de lectura.
  
Cuando se establece la marca SUPPRESS_RECEIPT:
  
- Si MSGFLAG_READ ya está establecido, no haga nada. 
    
- Si no se establece MSGFLAG_READ, configurarla y cancelarlas pendientes informes de lectura.
    
Cuando se establece la marca CLEAR_READ_FLAG, desactive la marca MSGFLAG_READ en propiedad **PR_MESSAGE_FLAGS** de cada mensaje y no enviar los informes de lectura. 
  
Cuando se establece la marca GENERATE_RECEIPT_ONLY, envíe los informes de lectura pendientes. Hacer MSGFLAG_READ no establecer o borrar.
  
Cuando se establecen los indicadores de la SUPPRESS_RECEIPT y la GENERATE_RECEIPT_ONLY, establezca la propiedad PR_READ_RECEIPT_REQUESTED de MAPI en FALSE si se configura y no enviar un informe de lectura.
  
Puede optimizar el comportamiento de informe mediante la supresión de la generación de informes de lectura en determinadas condiciones. Sin embargo, si no se admiten la supresión de informes y un cliente llama a **SetReadFlag** con el conjunto de marca SUPPRESS_RECEIPT, devolver MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI usa el método **IMessage::SetReadFlag** para establecer marcas de lectura en los mensajes seleccionados.  <br/> |
   
## <a name="see-also"></a>Vea también

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

