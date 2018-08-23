---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 88185efea344844016547d0844277de6e0d661db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578321"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece o borra el indicador MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uno o varios de los mensajes de la carpeta y administra el envío de informes de lectura. 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

_lpMsgList_
  
> [entrada] Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que identifican el mensaje o los mensajes que han leído marcas para activar o desactivar. Si _lpMsgList_ se establece en NULL, la lectura marcas para todos los mensajes de la carpeta se establece o desactivados. 
    
_ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. El parámetro _ulUIParam_ se omite a menos que se establece la marca MESSAGE_DIALOG en el parámetro _ulFlags indicado_ . 
    
_lpProgress_
  
> [entrada] Un puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacén de mensajes muestra un indicador de progreso mediante la implementación de MAPI. El parámetro _lpProgress_ se omite a menos que se establece la marca MESSAGE_DIALOG en _ulFlags_.
    
_ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla la configuración de indicador de lectura de un mensaje y el procesamiento de informes de lectura. Se pueden establecer los siguientes indicadores:
    
  - CLEAR_READ_FLAG: Se debe borrar la marca MSGFLAG_READ en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de lectura. 
        
  - CLEAR_NRN_PENDING: Se debe borrar la marca MSGFLAG_NRN_PENDING en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de no leído. 
        
  - CLEAR_RN_PENDING: Se debe borrar la marca MSGFLAG_RN_PENDING en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de lectura. 
        
  - GENERATE_RECEIPT_ONLY: Se debe enviar un informe de lectura si uno está pendiente, pero no debe haber ningún cambio en el estado de la marca MSGFLAG_READ.
        
  - MAPI_DEFERRED_ERRORS: Permite **SetReadFlags** devolver de correctamente, posiblemente antes de que la operación ha finalizado. 
        
  - MESSAGE_DIALOG: Muestra un indicador de progreso mientras se realiza la operación.
    
  - SUPPRESS_RECEIPT: Se debe cancelar un informe de lectura pendiente si se solicita un informe de lectura y esta llamada cambia el estado del mensaje de no leído a leer. Si esta llamada no cambia el estado del mensaje, el proveedor de almacenamiento de mensajes puede pasar por alto esta marca.
    
## <a name="return-values"></a>Valores devueltos

S_OK 
  
> El indicador de lectura para el mensaje especificado o los mensajes se ha establecido correctamente o se desactiva.
    
MAPI_E_NO_SUPPRESS 
  
> El proveedor de almacén de mensajes no es compatible con la supresión de informes de lectura.
    
MAPI_E_INVALID_PARAMETER 
  
> Una de las siguientes combinaciones incompatibles de flags se establece en el parámetro _ulFlags indicado_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todos los mensajes se han procesado correctamente. Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta. Para probar esta advertencia, utilice la macro **HR_FAILED** . Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder::SetReadFlags** establece o borra el indicador MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** de uno o varios de los mensajes de la carpeta. Establecer el indicador MSGFLAG_READ marca un mensaje como lectura, que no necesariamente indica que el destinatario realmente ha leído el mensaje. 
  
**SetReadFlags** también administra el envío de informes de lectura. 
  
No se puede cambiar la marca de lectura para los siguientes elementos:
  
- Mensajes que no existen.
    
- Los mensajes que se han moverán a otro lugar.
    
- Mensajes que están abiertos con permiso de lectura y escritura.
    
- Mensajes que se envían actualmente.
    
## <a name="notes-to-implementers"></a>Notas para los implementadores

Puede decidir no compatible con el envío de informes de lectura y la solicitud para suprimir informes de lectura. Para evitar la eliminación de un informe de lectura, devolver MAPI_E_NO_SUPPRESS cuando se llama a **SetReadFlags** con SUPPRESS_RECEIPT establecido en el parámetro _ulFlags indicado_ . 
  
Cuando el parámetro _lpMsgList_ apunta a más de un mensaje, realizar la operación más completo posible para cada mensaje. No detiene la operación de forma prematura a menos que se produzca un error que está fuera de su control, como la falta de memoria, está quedando sin espacio en disco o daños en el almacén de mensajes. 
  
Si ninguno de los indicadores se establecen en el parámetro _ulFlags_ , se aplican las siguientes reglas: 
  
- Si MSGFLAG_READ ya está establecido, no haga nada.
    
- Si no se establece MSGFLAG_READ, establézcalo inmediatamente y enviarlas pendientes informes de lectura si se establece la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).
    
Cuando se establece la marca SUPPRESS_RECEIPT, se aplican las siguientes reglas:
  
- Si MSGFLAG_READ ya está establecido, no haga nada. 
    
- Si no se establece MSGFLAG_READ, configurarla y cancelarlas pendientes informes de lectura.
    
Cuando se establece la marca CLEAR_READ_FLAG, desactive la marca MSGFLAG_READ en propiedad **PR_MESSAGE_FLAGS** de cada mensaje y no enviar los informes de lectura. 
  
Cuando se establece la marca GENERATE_RECEIPT_ONLY, envíe los informes de lectura pendientes. Hacer MSGFLAG_READ no establecer o borrar.
  
Cuando se establecen los indicadores de la SUPPRESS_RECEIPT y la GENERATE_RECEIPT_ONLY, establecer **PR_READ_RECEIPT_REQUESTED de MAPI** en FALSE si se configura y no enviar un informe de lectura. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espera a que estos valores devueltos en las siguientes condiciones.
  
|**Condición**|**Valor devuelto**|
|:-----|:-----|
|**SetReadFlags** procesadas correctamente todos los mensajes.  <br/> |S_OK  <br/> |
|**SetReadFlags** no pudo procesar correctamente todos los mensajes.  <br/> |MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** no pudo completar.  <br/> |Cualquier valor de error excepto MAPI_E_NOT_FOUND  <br/> |
   
Cuando **SetReadFlags** es no se puede completar, no asuma que se ha realizado ningún trabajo. **SetReadFlags** es posible que han sido capaces establecer o borrar la marca MSGFLAG_READ para uno o varios de los mensajes antes de encontrar el error. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI usa el método **IMAPIFolder::SetReadFlags** para establecer manualmente el estado de lectura en los mensajes especificados.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Propiedad canónica PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)  
- [Uso de macros para el control de errores](using-macros-for-error-handling.md)

