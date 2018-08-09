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
ms.openlocfilehash: e2871f5804cda172328fbd3ebdc43f860de939ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817761"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**Hace referencia a**: Outlook 
  
Intenta quitar un mensaje de la cola de salida.
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [entrada] Un puntero al identificador de entrada del mensaje para quitar de la cola de salida. 
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El mensaje se quitó correctamente de la cola de salida.
    
MAPI_E_NOT_IN_QUEUE 
  
> El mensaje identificado por _lpEntryID_ ya no está en la cola de salida del almacén de mensajes, normalmente porque ya se ha enviado. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> El mensaje identificado por _lpEntryID_ está bloqueado por la cola MAPI y no se puede anular la operación. 
    
## <a name="remarks"></a>Comentarios

El método **IMsgStore::AbortSubmit** intenta quitar un mensaje enviado desde la cola de salida del almacén de mensajes. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Una vez que se envía un mensaje, anulando el envío mediante una llamada a **AbortSubmit** es la única acción que se puede realizar en el mensaje. No se espera **AbortSubmit** siempre se realice correctamente. Dependiendo de cómo se implementa el sistema de mensajería subyacente, no sería posible cancelar el envío del mensaje. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |MFCMAPI usa el método **IMsgStore::AbortSubmit** para anular el envío del mensaje seleccionado.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

