---
title: Enviar mensajes usando proveedores de almacenamiento de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b34714a230adb44417624d149d34ed6a14a2dfa5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437612"
---
# <a name="sending-messages-by-using-message-store-providers"></a>Enviar mensajes usando proveedores de almacenamiento de mensajes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de al almacenamiento de mensajes no son necesarios para admitir envíos de mensajes salientes (es decir, la capacidad de las aplicaciones cliente de usar el proveedor de almacenamiento de mensajes para enviar mensajes). Las aplicaciones cliente necesitan usar un almacén de mensajes al enviar mensajes, ya que los datos del mensaje deben almacenarse en algún lugar entre el momento en que el usuario termina de redactarlo y el momento en que la cola MAPI proporciona el mensaje a un proveedor de transporte para su envío al sistema de mensajería subyacente. Si el proveedor del almacén de mensajes no admite envíos de mensajes salientes, no se puede usar como almacén de mensajes predeterminado.
  
Para admitir el envío de mensajes, el proveedor del almacén de mensajes debe hacer lo siguiente:
  
- Implementar una cola de mensajes salientes.
    
- Admite el [método IMessage::SubmitMessage](imessage-submitmessage.md) en objetos de mensaje creados en el almacén de mensajes. 
    
- Admite los métodos **IMsgStore** específicos de la cola MAPI: [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)e [IMsgStore::SetLockState](imsgstore-setlockstate.md).
    
El **método SetLockState** es importante para la interoperación correcta entre la cola MAPI y los clientes. Cuando la cola MAPI llama a **SetLockState** en un mensaje saliente, el proveedor del almacén de mensajes no debe permitir que los clientes abran el mensaje. Si un cliente intenta abrir un mensaje bloqueado por la cola MAPI, el proveedor del almacén de mensajes debe devolver MAPI_E_NO_ACCESS. El estado bloqueado de un mensaje no tiene que ser persistente en caso de que el almacén se cierre mientras el mensaje está bloqueado por la cola MAPI. 
  
Independientemente de si la cola MAPI ha bloqueado un mensaje saliente, el proveedor de almacenamiento de mensajes no debe permitir que se abra un mensaje en la cola de mensajes salientes para su escritura. Si un cliente llama al método [IMSgStore::OpenEntry](imsgstore-openentry.md) en un mensaje saliente con la marca MAPI_MODIFY, la llamada debe producir un error y devolver MAPI_E_SUBMITTED. Si una aplicación cliente llama a **OpenEntry** en un mensaje saliente con la marca MAPI_BEST_ACCESS, el proveedor del almacén de mensajes debe permitir el acceso de solo lectura al mensaje. 
  
Cuando un mensaje se va a controlar mediante la cola MAPI, el proveedor del almacén de mensajes establece la propiedad **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) del mensaje en SUBMITFLAG_LOCKED. El SUBMITFLAG_LOCKED indica que la cola MAPI ha bloqueado el mensaje para su uso exclusivo. El otro valor para **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, se establece cuando el mensaje requiere preprocesamiento por una o varias funciones de preprocesador registradas por un proveedor de transporte.
  
Los procedimientos siguientes describen cómo interactúan el almacén de mensajes, el transporte y la cola MAPI para enviar un mensaje desde un cliente a uno o más destinatarios. 
  
La aplicación cliente llama al [método IMessage::SubmitMessage.](imessage-submitmessage.md) En **SubmitMessage,** el proveedor del almacén de mensajes hace lo siguiente:
  
1. Llama [a IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md). Si MAPI devuelve un error, el proveedor del almacén de mensajes devuelve ese error al cliente.
    
2. Establece el MSGFLAG_SUBMIT bit en la **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje.
    
3. Garantiza que hay una columna para la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) en la tabla de destinatarios y la establece en FALSE para indicar que ningún transporte ha asumado la responsabilidad de transmitir el mensaje.
    
4. Establece la fecha y la hora de origen en **la PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Llama [a IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) para hacer lo siguiente: 
    
    1. Expanda todas las listas de distribuci�n personal y destinatarios personalizados y reemplace todos los nombres de presentaci�n que ha cambiado con sus nombres originales.
        
    2. Quite los nombres duplicados.
        
    3. Compruebe si hay preprocesamiento necesario y, si es necesario, establezca la marca NEEDS_PREPROCESSING y la propiedad **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), que está reservada para MAPI. 
        
    4. Establecer el indicador NEEDS_SPOOLER si el almac�n de mensajes se complementa con un transporte y no puede controlar todos los destinatarios. 
    
6. Si se establece la marca de mensaje NEEDS_PREPROCESSING, realiza las tareas siguientes:
    
    1. Coloca el mensaje en la cola saliente con el SUBMITFLAG_PREPROCESS bit establecido en la **PR_SUBMIT_FLAGS** propiedad. 
        
    2. Notifica a la cola MAPI que ha cambiado la cola.
        
    3. Devuelve el control al cliente y contin�a el flujo de mensajes en la cola MAPI. La cola MAPI realiza las tareas siguientes: 
    
       1. Bloquea el mensaje llamando a [IMsgStore::SetLockState](imsgstore-setlockstate.md).
            
       2. Realiza el preprocesamiento necesario llamando a todas las funciones de preprocesamiento en el orden de registro. Los proveedores de transporte [llaman a IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar funciones de preprocesamiento. 
            
       3. Llama [a IMessage::SubmitMessage](imessage-submitmessage.md) en el mensaje abierto para indicar al almacén de mensajes que el preprocesamiento se ha completado. 
    
Si no había preprocesamiento o había preprocesamiento y la cola MAPI denominada **SubmitMessage**, el proveedor del almacén de mensajes hace lo siguiente en el proceso de cliente: 
  
- Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Administra a todos los destinatarios que pueden administrar.
    
   - Establece la propiedad **PR_RESPONSIBILITY** en TRUE para todos los destinatarios que administra. 
    
   - Si todos los destinatarios se conocen en este almac�n de acoplamiento ajustado y transporte, realiza las tareas siguientes: 
    
     - Llama [a IMAPISupport::CompleteMsg](imapisupport-completemsg.md) si el mensaje se preprocesó o el proveedor del almacén de mensajes desea que la cola MAPI complete el procesamiento de mensajes. El flujo de mensajes continúa con la cola MAPI. 
    
     - Realiza las siguientes tareas si el mensaje no se preprocesó o si el proveedor del almacén de mensajes no desea que la cola MAPI complete el procesamiento de mensajes:
    
       1. Copia el mensaje en la carpeta identificada por el identificador de entrada en **la propiedad PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), si se establece.
            
       2. Elimina el mensaje si la **propiedad PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) se ha establecido en TRUE.
            
       3. Desbloquea el mensaje si está bloqueado.
            
       4. Devuelve al cliente. El flujo de mensajes se ha completado.
    
  - Realiza las siguientes tareas si el mensaje se preprocesó o si el proveedor desea que la cola MAPI complete el procesamiento de mensajes:
    
    1. Llama [a IMAPISupport::CompleteMsg](imapisupport-completemsg.md). 
          
    2. Continúa el flujo de mensajes con la cola MAPI. Para obtener más información, vea [Enviar mensajes: Tareas de cola MAPI](sending-messages-mapi-spooler-tasks.md).
    
  - Realiza las siguientes tareas si el mensaje no se preprocesó o el proveedor no desea que la cola complete el procesamiento de mensajes:
    
    1. Copia el mensaje en la carpeta identificada por el identificador de entrada en **PR_SENTMAIL_ENTRYID** propiedad, si se establece. 
        
    2. Elimina el mensaje si la **PR_DELETE_AFTER_SUBMIT** se ha establecido en TRUE. 
        
    3. Desbloquea el mensaje si está bloqueado. 
        
    4. Devuelve al autor de la llamada. El flujo de mensajes se ha completado.
    
- Si el almac�n de mensajes no est� estrechamente asociado a un transporte, no todos los destinatarios eran conocidos para el almac�n de mensajes o se establece la marca NEEDS_SPOOLER, realiza las tareas siguientes:
    
  1. Coloca el mensaje en la cola de salida sin establecer el bit SUBMITFLAG_PREPROCESS en la propiedad **PR_SUBMIT_FLAGS**. 
    
  2. Notifica a la cola MAPI que ha cambiado la cola de salida al generar una notificaci�n de la tabla. 
    
  3. Devuelve al cliente y el flujo de mensajes contin�a con un conjunto de tareas que se realizan por la cola MAPI.
    
## <a name="see-also"></a>Consulte también

- [Caracter�sticas de almac�n de mensajes](message-store-features.md)

