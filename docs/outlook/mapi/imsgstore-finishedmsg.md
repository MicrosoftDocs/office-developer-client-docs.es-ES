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
ms.openlocfilehash: 8b15f12c9a7ac2041c895b935098f9681e4b3a3c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589955"
---
# <a name="imsgstorefinishedmsg"></a>IMsgStore::FinishedMsg

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite que el proveedor de almacén de mensajes realizar el procesamiento en un mensaje enviado. Se llama a este m�todo s�lo por la cola MAPI.
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del mensaje que va a procesar.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Procesamiento en el mensaje enviado era correcta.
    
MAPI_E_NO_SUPPORT 
  
> El proveedor de almacén de mensajes no es compatible con el procesamiento del mensaje enviado. Este valor de error se devuelve si el autor de la llamada no es la cola de MAPI.
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore::FinishedMsg** realiza procesamiento en un mensaje enviado. Este proceso puede implicar eliminar el mensaje, mover a una carpeta diferente, o ambas acciones. El tipo de procesamiento depende de si se establecen las propiedades de **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) y **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)). 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

En la implementación de **FinishedMsg**, desbloquee el mensaje identificado por _lpEntryID_ y realizar el procesamiento adecuado. Siempre se bloqueará el mensaje de destino; la cola MAPI nunca pasa el identificador de entrada para un mensaje desbloqueado a **FinishedMsg**.
  
Es posible que ni se establece **PR_DELETE_AFTER_SUBMIT** o **PR_SENTMAIL_ENTRYID** , ambos se establecen o se establece uno u otro. En la siguiente tabla se describe la acción que debe realizar en función de la configuración: 
  
|||
|:-----|:-----|
|Si se establece ninguna de estas propiedades:  <br/> |Dejar el mensaje en la carpeta desde la que se envió (normalmente, la Bandeja de salida).  <br/> |
|Si se establecen las dos propiedades:  <br/> |Mover el mensaje a la carpeta indicada, si así lo desea y, a continuación, elimínela.  <br/> |
|Si se establece PR_SENTMAIL_ENTRYID:  <br/> |Mover el mensaje a la carpeta indicada.  <br/> |
|Si se establece PR_DELETE_AFTER_SUBMIT:  <br/> |Eliminar el mensaje.  <br/> |
   
Después de haber tomado cualquier acción es adecuada, llame al método [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) . 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPISupport::DoSentMail](imapisupport-dosentmail.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

