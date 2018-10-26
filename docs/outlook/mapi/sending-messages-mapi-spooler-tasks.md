---
title: Env�o de mensajes Tareas de cola de impresi�n MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: eef65990637d9c164ffe75f682e01ed134510e32
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570278"
---
# <a name="sending-messages-mapi-spooler-tasks"></a>Env�o de mensajes: Tareas de cola de impresi�n MAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
La cola MAPI est� implicada en el proceso de transmisi�n de mensajes cuando el almac�n de mensajes no est� asociado estrechamente con un proveedor de transporte, cuando el almac�n de acoplamiento ajustado y el transporte no pueden tratar un destinatario y cuando el mensaje requiere preprocesamiento.
  
 **Despu�s de cualquier preprocesamiento es necesario, la cola MAPI realiza los siguientes pasos:**
  
1. If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method. 
    
2. Tiene el proveedor de transporte para enviar el mensaje a todos los destinatarios que tienen su propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) establecida en FALSE. 
    
3. Llama a la función apropiada ([RemovePreprocessInfo](removepreprocessinfo.md)) para limpiar cualquier información adicional que se agregó al mensaje para su uso durante el preprocesamiento de si se ha establecido la propiedad **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)). This function is specified when the transport provider registers its preprocessor function. 
    
4. Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:
    
  - Desbloquea el mensaje.
    
  - Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists. A continuación, copia el mensaje a la carpeta identificada por el identificador de entrada en la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), si no se ha reemplazado por una mensajería proveedor de enlace del envía el procesamiento de mensajes. Por último, elimina el mensaje si la propiedad **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) se ha establecido en TRUE. 
    

