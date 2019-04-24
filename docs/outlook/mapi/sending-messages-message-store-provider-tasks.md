---
title: Env�o de mensajes Tareas de proveedor de almac�n de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: acbfd3ae-bfdc-4103-bed2-6bcf7b9c448c
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: b65113e59b236b1f13596627a8669ae458f76369
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338433"
---
# <a name="sending-messages-message-store-provider-tasks"></a>Enviar mensajes: tareas de proveedor de almacén de mensajes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
A message store provider gets involved with the message sending process when a client calls the message's [IMessage::SubmitMessage](imessage-submitmessage.md) method. If multiple messages are to be sent, the message store must send them in the same order that the client used for its **SubmitMessage** calls. 
  
El proveedor de almacenamiento de mensajes determina si se debe o no relacionadas con la cola MAPI. Si no se complementa el proveedor de almacenamiento de mensajes, el mensaje requiere preprocesamiento, o el almac�n de acoplamiento ajustado y el transporte no pueden controlar todos los destinatarios, la cola MAPI debe estar involucrada. 
  
El procedimiento siguiente describe las tareas necesarias de un proveedor de almac�n de mensajes para enviar un mensaje. 
  
**En IMessage:: SubmitMessage, el proveedor de almacenamiento de mensajes**:
  
1. Llama a [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md) si el mensaje tiene la marca MSGFLAG_RESEND establecida en su propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) y devuelve cualquier error al cliente. **PrepareSubmit** comprueba la propiedad **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de todos los destinatarios de la lista de destinatarios del mensaje.
    
   - Si se establece la marca MAPI_SUBMITTED, que indica que el destinatario no recibió el mensaje original, **PrepareSubmit** borra la marca y establece la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) en true. 
    
   - Si no se establece la marca MAPI_SUBMITTED, que indica que el destinatario haya recibido el mensaje original, **PrepareSubmit** cambia la propiedad **PR_RECIPIENT_TYPE** a MAPI_P1 y establece la propiedad **PR_RESPONSIBILITY** como TRUE y devuelve cualquier error generado por **PrepareSubmit** al cliente. 
    
2. Establece el indicador MSGFLAG_SUBMIT en la propiedad del mensaje **PR_MESSAGE_FLAGS**. 
    
3. Se asegura de que hay una columna para **PR_RESPONSIBILITY** en la tabla de destinatarios y establece en FALSE para indicar que no hay transporte tiene de responsabilidad supuesta a�n para transmitir el mensaje. 
    
4. Establece la fecha y la hora de origen en la propiedad **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Calls [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) to: 
    
   - Expanda todas las listas de distribuci�n personal y destinatarios personalizados y reemplace todos los nombres de presentaci�n que ha cambiado con sus nombres originales.
   - Quite los nombres duplicados.
   - Compruebe si el preprocesamiento es necesario y, si es necesario, establezca la marca NEEDS_PREPROCESSING y la propiedad **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), una propiedad reservada para MAPI. 
   - Establecer el indicador NEEDS_SPOOLER si el almac�n de mensajes se complementa con un transporte y no puede controlar todos los destinatarios. 
    
6. Si se establece la marca de mensaje NEEDS_PREPROCESSING, realiza las tareas siguientes:
    
   - Coloca el mensaje en la cola de salida con el bit SUBMITFLAG_PREPROCESS establecido en la propiedad **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)).
   - Notifica a la cola MAPI que ha cambiado la cola.
   - Devuelve el control al cliente y contin�a el flujo de mensajes en la cola MAPI. 
   - La cola MAPI realiza las tareas siguientes:
     - Bloquea el mensaje mediante una llamada a IMsgStore:: SetLockState. 
     - Realiza el preprocesamiento necesario llamando a todas las funciones de preprocesamiento en el orden de registro. Los proveedores de transporte llaman a IMAPISupport:: RegisterPreprocessor para registrar las funciones de preprocesamiento. 
     - Llama a IMessage:: SubmitMessage en el mensaje abierto para indicar al almacén de mensajes que el preprocesamiento se ha completado.

<br/>

Los dos pasos siguientes se producen en el proceso de cliente si no había preprocesamiento y cuando la cola MAPI llama a **SubmitMessage** si se estaba preprocesando. 

**El proveedor del almacén de mensajes**:

1. Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Administra a todos los destinatarios que pueden administrar.
   - Establece la propiedad **PR_RESPONSIBILITY** en TRUE para todos los destinatarios que administra. 
   - Si todos los destinatarios se conocen en este almac�n de acoplamiento ajustado y transporte, realiza las tareas siguientes:
     - Llama a IMAPISupport:: CompleteMsg si el mensaje estaba preprocesado o el proveedor de almacén de mensajes desea que la cola MAPI complete el procesamiento de mensajes, lo que se recomienda para que se puedan invocar los enlaces de mensajería. El flujo de mensajes sigue con la cola MAPI como se describe en el siguiente procedimiento.  
     - Realiza las siguientes tareas si el mensaje no se ha preprocesado o si el proveedor de almacenamiento de mensajes no desea que la cola MAPI finalice el procesamiento de mensajes:
       - Copia el mensaje en la carpeta identificada por el identificador de entrada en la propiedad PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId), si se ha establecido.
       - Elimina el mensaje si la propiedad PR_DELETE_AFTER_SUBMIT (PidTagDeleteAfterSubmit) se ha establecido en TRUE.
       - Desbloquea el mensaje si está bloqueado.
       - Devuelve al cliente. El flujo de mensajes se ha completado. 
   
2. Si el almac�n de mensajes no est� estrechamente asociado a un transporte, no todos los destinatarios eran conocidos para el almac�n de mensajes o se establece la marca NEEDS_SPOOLER, realiza las tareas siguientes:
    
   - Coloca el mensaje en la cola de salida sin establecer el bit SUBMITFLAG_PREPROCESS en la propiedad **PR_SUBMIT_FLAGS**. 
   - Notifica a la cola MAPI que ha cambiado la cola de salida al generar una notificaci�n de la tabla. 
   - Devuelve al cliente y el flujo de mensajes contin�a con un conjunto de tareas que se realizan por la cola MAPI.
    
Cuando un mensaje gestione la cola MAPI, el proveedor de almacenamiento de mensajes, establece la propiedad del mensaje **PR_SUBMIT_FLAGS** a SUBMITFLAG_LOCKED. El indicador SUBMITFLAG_LOCKED indica que la cola MAPI ha bloqueado el mensaje para su uso exclusivo. El otro valor para **PR_SUBMIT_FLAGS,** SUBMITFLAG_PREPROCESS, se establece cuando el mensaje requiere preprocesamiento por una o m�s funciones del preprocesador registradas por un proveedor de transporte. 
  

