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
  
Establece o borra la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uno o más de los mensajes de la carpeta y administra el envío de informes de lectura. 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

_lpMsgList_
  
> a Un puntero a una matriz de estructuras [ENTRYLIST](entrylist.md) que identifican el mensaje o los mensajes que tienen marcas de lectura para establecer o borrar. Si _lpMsgList_ se establece en null, se establecen o borran las marcas de lectura de todos los mensajes de la carpeta. 
    
_ulUIParam_
  
> a Identificador de la ventana primaria del indicador de progreso. El parámetro _ulUIParam_ se omite a menos que se establezca la marca MESSAGE_DIALOG en el parámetro _ulFlags_ . 
    
_lpProgress_
  
> a Un puntero a un objeto Progress que muestra un indicador de progreso. Si se pasa NULL en _lpProgress_, el proveedor de almacenamiento de mensajes muestra un indicador de progreso mediante la implementación de MAPI. El parámetro _lpProgress_ se omite a menos que se establezca la marca MESSAGE_DIALOG en _ulFlags_.
    
_ulFlags_
  
> a Máscara de máscara de marcadores que controla la configuración del indicador de lectura de un mensaje y el procesamiento de los informes de lectura. Se pueden establecer los siguientes indicadores:
    
  - CLEAR_READ_FLAG: la marca MSGFLAG_READ se debe borrar en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de lectura. 
        
  - CLEAR_NRN_PENDING: la marca MSGFLAG_NRN_PENDING se debe borrar en **PR_MESSAGE_FLAGS** y no se debe enviar un informe no leído. 
        
  - CLEAR_RN_PENDING: la marca MSGFLAG_RN_PENDING se debe borrar en **PR_MESSAGE_FLAGS** y no se debe enviar un informe de lectura. 
        
  - GENERATE_RECEIPT_ONLY: se debe enviar un informe de lectura si hay uno pendiente, pero no debe haber ningún cambio en el estado de la marca MSGFLAG_READ.
        
  - MAPI_DEFERRED_ERRORS: permite que **SetReadFlags** se devuelva correctamente, posiblemente antes de que se haya completado la operación. 
        
  - MESSAGE_DIALOG: muestra un indicador de progreso mientras se lleva a cabo la operación.
    
  - SUPPRESS_RECEIPT: se debe cancelar un informe de lectura pendiente si se ha solicitado un informe de lectura y esta llamada cambia el estado del mensaje de no leído a leído. Si esta llamada no cambia el estado del mensaje, el proveedor del almacén de mensajes puede omitir esta marca.
    
## <a name="return-values"></a>Valores devueltos

S_OK 
  
> La marca de lectura del mensaje o mensajes especificados se estableció o borró correctamente.
    
MAPI_E_NO_SUPPRESS 
  
> El proveedor de almacenamiento de mensajes no admite la supresión de informes de lectura.
    
MAPI_E_INVALID_PARAMETER 
  
> Una de las siguientes combinaciones incompatibles de indicadores se establece en el parámetro _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> La llamada se realizó correctamente, pero no todos los mensajes se procesaron correctamente. Cuando se devuelve esta advertencia, la llamada se debe administrar como correcta. Para probar esta advertencia, use la macro **HR_FAILED** . Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentarios

El método **IMAPIFolder:: SetReadFlags** establece o borra la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** de uno o más de los mensajes de la carpeta. Si se establece la marca MSGFLAG_READ, se marca un mensaje como leído, que no indica necesariamente que el destinatario previsto haya leído el mensaje en realidad. 
  
**SetReadFlags** también administra el envío de informes de lectura. 
  
No se puede cambiar la marca de lectura para lo siguiente:
  
- Mensajes que no existen.
    
- Mensajes que se movieron en otro lugar.
    
- Mensajes que están abiertos con permiso de lectura y escritura.
    
- Mensajes que se envían actualmente.
    
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede decidir no admitir el envío de informes de lectura y la solicitud para suprimir informes de lectura. Para evitar la supresión de un informe de lectura, devuelva MAPI_E_NO_SUPPRESS cuando se llame a **SetReadFlags** con SUPPRESS_RECEIPT establecido en el parámetro _ulFlags_ . 
  
Cuando el parámetro _lpMsgList_ apunta a más de un mensaje, realice la operación lo más completamente posible para cada mensaje. No detenga la operación prematuramente a menos que se produzca un error que esté más allá del control, como la falta de memoria, la falta de espacio en disco o que esté dañada en el almacén de mensajes. 
  
Si no se establece ninguno de los indicadores en el parámetro _ulFlags_ , se aplican las siguientes reglas: 
  
- Si MSGFLAG_READ ya está establecido, no haga nada.
    
- Si no se establece MSGFLAG_READ, establézcalo inmediatamente y envíe los informes de lectura pendientes si se establece la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).
    
Cuando se establece la marca SUPPRESS_RECEIPT, se aplican las siguientes reglas:
  
- Si MSGFLAG_READ ya está establecido, no haga nada. 
    
- Si no se establece MSGFLAG_READ, establézcalo y cancele los informes de lectura pendientes.
    
Cuando se establece la marca CLEAR_READ_FLAG, borre la marca MSGFLAG_READ en la propiedad **PR_MESSAGE_FLAGS** de cada mensaje y no envíe ningún informe de lectura. 
  
Cuando se establece la marca GENERATE_RECEIPT_ONLY, enviar los informes de lectura pendientes. No establezca ni borre MSGFLAG_READ.
  
Cuando se establecen las dos marcas SUPPRESS_RECEIPT y GENERATE_RECEIPT_ONLY, se establece **PR_READ_RECEIPT_REQUESTED** en false si se establece y no se envía un informe de lectura. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Espere estos valores devueltos en las siguientes condiciones.
  
|**Condición**|**Valor devuelto**|
|:-----|:-----|
|**SetReadFlags** ha procesado correctamente todos los mensajes.  <br/> |S_OK  <br/> |
|**SetReadFlags** no pudo procesar correctamente todos los mensajes.  <br/> |MAPI_W_PARTIAL_COMPLETION o MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** no se pudo completar.  <br/> |Cualquier valor de error excepto MAPI_E_NOT_FOUND  <br/> |
   
Cuando **SetReadFlags** no pueda completarse, no dé por supuesto que no se ha realizado ningún trabajo. Es posible que **SetReadFlags** haya podido establecer o borrar la marca MSGFLAG_READ para uno o más de los mensajes antes de que se produzca el error. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnSetReadFlag  <br/> |MFCMAPI usa el método **IMAPIFolder:: SetReadFlags** para establecer manualmente el estado de lectura de los mensajes especificados.  <br/> |
   
## <a name="see-also"></a>Ver también

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Propiedad canónica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Propiedad canónica PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)  
- [Uso de macros para el control de errores](using-macros-for-error-handling.md)

