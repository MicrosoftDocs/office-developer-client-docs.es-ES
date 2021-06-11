---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427090"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite al proveedor del almacén de mensajes realizar el procesamiento en un mensaje enviado. Se llama a este m�todo s�lo por la cola MAPI.
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _cbEntryID_
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada del mensaje que se va a procesar.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El procesamiento en el mensaje enviado se ha realizado correctamente.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor del almacén de mensajes no admite el procesamiento de mensajes enviados. Este valor de error se devuelve si el autor de la llamada no es la cola MAPI.
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::FinishedMsg** realiza el procesamiento en un mensaje enviado. Este procesamiento puede implicar eliminar el mensaje, moverlo a una carpeta diferente o ambas acciones. El tipo de procesamiento depende de si se establecen las propiedades **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) y **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

En la implementación de **FinishedMsg,** desbloquea el mensaje identificado por  _lpEntryID_ y realiza el procesamiento adecuado. El mensaje de destino siempre estará bloqueado; la cola MAPI nunca pasa el identificador de entrada de un mensaje desbloqueado a **FinishedMsg**.
  
Es posible que no **se PR_DELETE_AFTER_SUBMIT** o **PR_SENTMAIL_ENTRYID,** ambos están establecidos o se establece uno u otro. En la tabla siguiente se describe la acción que debe realizar en función de la configuración: 
  
|||
|:-----|:-----|
|Si no se establece ninguna propiedad:  <br/> |Deje el mensaje en la carpeta desde la que se envió (normalmente, la Bandeja de salida).  <br/> |
|Si se establecen ambas propiedades:  <br/> |Mueva el mensaje a la carpeta indicada, si lo desea, y, a continuación, elimínelo.  <br/> |
|Si PR_SENTMAIL_ENTRYID está establecido:  <br/> |Mueva el mensaje a la carpeta indicada.  <br/> |
|Si PR_DELETE_AFTER_SUBMIT está establecido:  <br/> |Elimine el mensaje.  <br/> |
   
Después de realizar cualquier acción que sea apropiada, llame al método [IMAPISupport::D oSentMail.](imapisupport-dosentmail.md) 
  
## <a name="see-also"></a>Vea también



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

