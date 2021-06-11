---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414385"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Intenta quitar un mensaje de la cola saliente.
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada del mensaje que se quitará de la cola saliente. 
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje se quitó correctamente de la cola saliente.
    
MAPI_E_NOT_IN_QUEUE 
  
> El mensaje identificado por  _lpEntryID_ ya no está en la cola de salida del almacén de mensajes, normalmente porque ya se ha enviado. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> El mensaje identificado por  _lpEntryID_ está bloqueado por la cola MAPI y la operación no se puede abortar. 
    
## <a name="remarks"></a>Comentarios

El **método IMsgStore::AbortSubmit** intenta quitar un mensaje enviado de la cola saliente del almacén de mensajes. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Después de enviar un mensaje, anular el envío llamando a **AbortSubmit** es la única acción que se puede realizar en el mensaje. No espere que **AbortSubmit** siempre se realice correctamente. Según cómo se implemente el sistema de mensajería subyacente, es posible que no sea posible cancelar el envío del mensaje. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |MFCMAPI usa el **método IMsgStore::AbortSubmit** para anular el envío del mensaje seleccionado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

