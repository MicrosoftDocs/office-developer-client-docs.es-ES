---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 8289b8dd2e0ab3c760e77a37b821d2fe74e4abe9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423954"
---
# <a name="imapisupportdosentmail"></a>IMAPISupport::DoSentMail

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Procesa un mensaje enviado.
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpMessage_
  
> [entrada] Un puntero al mensaje abierto para el que se debe generar un mensaje en la carpeta designada para contener los elementos enviados.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.
  
 **DoSentMail** realiza las tareas siguientes: 
  
- Comprueba el mensaje de la **propiedad PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) para determinar si el mensaje debe eliminarse después del envío.
    
- Determina la ubicaci�n de la carpeta Elementos enviados.
    
- Inicia el enlace del mensaje de procesamiento para los enlaces definidos en la carpeta Elementos enviados.
    
- Mueve el mensaje a la carpeta Elementos enviados, la carpeta Elementos eliminados, o a otra carpeta.
    
- Libera el mensaje.
    
## <a name="see-also"></a>Vea también



[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[Propiedad can�nico de PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

