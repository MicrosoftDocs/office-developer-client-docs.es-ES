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
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406916"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece o borra la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uno o varios de los mensajes de la carpeta y administra el envío de informes de lectura. 
  
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
  
> [entrada] Puntero a una matriz de [estructuras ENTRYLIST](entrylist.md) que identifican el mensaje o los mensajes que tienen marcas de lectura para establecer o borrar. Si  _lpMsgList se_ establece en NULL, se establecen o borran las marcas de lectura de todos los mensajes de la carpeta. 
    
_ulUIParam_
  
> [entrada] Identificador de la ventana principal del indicador de progreso. El _parámetro ulUIParam_ se omite a menos que MESSAGE_DIALOG marca esté establecida en el _parámetro ulFlags._ 
    
_lpProgress_
  
> [entrada] Puntero a un objeto de progreso que muestra un indicador de progreso. Si se pasa NULL en  _lpProgress,_ el proveedor del almacén de mensajes muestra un indicador de progreso mediante la implementación de MAPI. El  _parámetro lpProgress_ se omite a menos que MESSAGE_DIALOG marca esté establecida en  _ulFlags_.
    
_ulFlags_
  
> [entrada] Máscara de bits de marcas que controla la configuración de la marca de lectura de un mensaje y el procesamiento de informes de lectura. Se pueden establecer las siguientes marcas:
    
  - CLEAR_READ_FLAG: la MSGFLAG_READ debe borrarse en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de lectura. 
        
  - CLEAR_NRN_PENDING: la MSGFLAG_NRN_PENDING debe borrarse en **PR_MESSAGE_FLAGS** y no se debe enviar un informe no leído. 
        
  - CLEAR_RN_PENDING: la MSGFLAG_RN_PENDING debe borrarse en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de lectura. 
        
  - GENERATE_RECEIPT_ONLY: se debe enviar un informe de lectura si hay uno pendiente, pero no debe haber ningún cambio en el estado de la marca MSGFLAG_READ lectura.
        
  - MAPI_DEFERRED_ERRORS: permite que **SetReadFlags** vuelva correctamente, posiblemente antes de que se complete la operación. 
        
  - MESSAGE_DIALOG: muestra un indicador de progreso mientras continúa la operación.
    
  - SUPPRESS_RECEIPT: se debe cancelar un informe de lectura pendiente si se ha solicitado un informe de lectura y esta llamada cambia el estado del mensaje de no leído a leído. Si esta llamada no cambia el estado del mensaje, el proveedor del almacén de mensajes puede omitir esta marca.
    
## <a name="return-values"></a>Valores devueltos

S_OK 
  
> La marca de lectura del mensaje o los mensajes especificados se estableció o despejado correctamente.
    
MAPI_E_NO_SUPPRESS 
  
> El proveedor del almacén de mensajes no admite la supresión de informes de lectura.
    
MAPI_E_INVALID_PARAMETER 
  
> Una de las siguientes combinaciones incompatibles de marcas se establece en el _parámetro ulFlags:_ 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se ha realizado correctamente, pero no todos los mensajes se han procesado correctamente. Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta. Para probar esta advertencia, use la **macro HR_FAILED** datos. Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentarios

El **método IMAPIFolder::SetReadFlags** establece o borra la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** de uno o varios de los mensajes de la carpeta. Al establecer MSGFLAG_READ marca un mensaje como leído, lo que no indica necesariamente que el destinatario deseado haya leído realmente el mensaje. 
  
**SetReadFlags** también administra el envío de informes de lectura. 
  
La marca de lectura no se puede cambiar para lo siguiente:
  
- Mensajes que no existen.
    
- Mensajes que se han movido a otro lugar.
    
- Mensajes abiertos con permiso de lectura y escritura.
    
- Mensajes que se envían actualmente.
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede decidir no admitir el envío de informes de lectura y la solicitud para suprimir los informes de lectura. Para evitar suprimir un informe de lectura, devuelva MAPI_E_NO_SUPPRESS cuando se llame a **SetReadFlags** con SUPPRESS_RECEIPT establecido en el _parámetro ulFlags._ 
  
Cuando el  _parámetro lpMsgList_ apunta a más de un mensaje, realice la operación lo más completa posible para cada mensaje. No detenga la operación antes de tiempo a menos que se produzca un error que esté fuera de su control, como que se queme la memoria, que se esté quedando sin espacio en disco o que el almacén de mensajes esté dañado. 
  
Si no se establece ninguna de las marcas en el  _parámetro ulFlags,_ se aplican las siguientes reglas: 
  
- Si MSGFLAG_READ ya está establecido, no haga nada.
    
- Si MSGFLAG_READ no está establecido, estapórelo inmediatamente y envíe los informes de lectura pendientes si se establece la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).
    
Cuando se SUPPRESS_RECEIPT marca, se aplican las siguientes reglas:
  
- Si MSGFLAG_READ ya está establecido, no haga nada. 
    
- Si MSGFLAG_READ no está establecido, estad léalo y cancele los informes de lectura pendientes.
    
Cuando se CLEAR_READ_FLAG marca, borre la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** de cada mensaje y no envíe ningún informe de lectura. 
  
Cuando se GENERATE_RECEIPT_ONLY marca, envíe los informes de lectura pendientes. No establecer ni borrar el MSGFLAG_READ.
  
Cuando se establecen SUPPRESS_RECEIPT y GENERATE_RECEIPT_ONLY, establezca **PR_READ_RECEIPT_REQUESTED** en FALSE si está establecido y no envíe un informe de lectura. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espere estos valores devueltos en las siguientes condiciones.
  
|**Condition**|**Valor devuelto**|
|:-----|:-----|
|**SetReadFlags** ha procesado correctamente todos los mensajes.  <br/> |S_OK  <br/> |
|**SetReadFlags** no pudo procesar correctamente todos los mensajes.  <br/> |MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** no se pudo completar.  <br/> |Cualquier valor de error excepto MAPI_E_NOT_FOUND  <br/> |
   
Cuando **SetReadFlags** no se puede completar, no suponga que no se ha realizado ningún trabajo. **Es posible que SetReadFlags** haya podido establecer o borrar la marca MSGFLAG_READ para uno o varios de los mensajes antes de encontrar el error. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI usa el **método IMAPIFolder::SetReadFlags** para establecer manualmente el estado de lectura en los mensajes especificados.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Propiedad canónica PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)  
- [Uso de macros para el control de errores](using-macros-for-error-handling.md)

