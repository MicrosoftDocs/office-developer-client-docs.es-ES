---
title: Envío de mensajes mediante el uso de mensaje de los proveedores de almacén
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: aaba816ca7efab6cee939087a18332561f31b81b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820619"
---
# <a name="sending-messages-by-using-message-store-providers"></a>Envío de mensajes mediante el uso de mensaje de los proveedores de almacén

**Hace referencia a**: Outlook 
  
Los proveedores de almacén de mensajes no son necesarios para admitir los envíos de mensajes salientes (es decir, la capacidad para las aplicaciones de cliente usar el proveedor de almacenamiento de mensajes para enviar mensajes). Las aplicaciones cliente que necesite utilizar un almacén de mensajes, mientras que el envío de mensajes, debido a que los datos del mensaje deben ser almacenados en algún lugar entre el momento en que el usuario haya terminado de redactar y la hora en que la cola MAPI proporciona el mensaje a un proveedor de transporte para envío al sistema de mensajería subyacente. Si su proveedor de almacén de mensajes no es compatible con los envíos de mensajes salientes, no se utiliza como almacén de mensajes predeterminado.
  
Para admitir el envío de mensajes, el proveedor de almacén de mensajes debe hacer lo siguiente:
  
- Implementar una cola de mensajes salientes.
    
- Admite el método [IMessage::SubmitMessage](imessage-submitmessage.md) en los objetos de mensajes creados en el almacén de mensajes. 
    
- Compatible con los métodos **IMsgStore** que son específicos de la cola MAPI: [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)y [IMsgStore::SetLockState](imsgstore-setlockstate.md).
    
El método **SetLockState** es importante para la interoperación adecuado entre los clientes y la cola de MAPI. Cuando la cola MAPI llama a **SetLockState** en un mensaje saliente, el proveedor de almacén de mensajes no debe permitir a los clientes abra el mensaje. Si un cliente intenta abrir un mensaje que está bloqueado por la cola MAPI, el proveedor de almacén de mensajes debe devolver MAPI_E_NO_ACCESS. El estado bloqueado de un mensaje no tiene que ser persistente en caso de que el almacén se cierra mientras el mensaje está bloqueado por la cola de MAPI. 
  
Independientemente de si la cola MAPI ha bloqueado un mensaje saliente, el proveedor de almacén de mensajes no debe permitir un mensaje en la cola de mensajes salientes que se abrirá para escribir en él. Si un cliente, llama al método [IMSgStore::OpenEntry](imsgstore-openentry.md) en un mensaje saliente con la marca MAPI_MODIFY, la llamada debe producir un error y devolver MAPI_E_SUBMITTED. Si una aplicación cliente llama **OpenEntry** en un mensaje saliente con la marca MAPI_BEST_ACCESS, el proveedor de almacenamiento de mensaje debe permitir acceso de sólo lectura para el mensaje. 
  
Cuando un mensaje se gestione la cola MAPI, el proveedor de almacén de mensajes establece la propiedad del mensaje **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) en SUBMITFLAG_LOCKED. El valor SUBMITFLAG_LOCKED indica que la cola MAPI ha bloqueado el mensaje para su uso exclusivo. El otro valor para **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, se establece cuando el mensaje requiere preprocesamiento por una o más funciones del preprocesador registradas por un proveedor de transporte.
  
Los procedimientos siguientes describen cómo interactúan el almacén de mensajes, el transporte y la cola MAPI para enviar un mensaje desde un cliente a uno o más destinatarios. 
  
La aplicación cliente llama al método de [IMessage::SubmitMessage](imessage-submitmessage.md) . En **SubmitMessage**, el proveedor de almacén de mensajes hace lo siguiente:
  
1. Llama a [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md). Si MAPI devuelve un error, el proveedor de almacenamiento de mensaje devuelve ese error al cliente.
    
2. Establece el bit en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje MSGFLAG_SUBMIT.
    
3. Se asegura de que hay una columna para la propiedad **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) en la tabla de destinatarios y establece en FALSE para indicar que no hay transporte aún ha asumido la responsabilidad para transmitir el mensaje.
    
4. Establece la fecha y hora de origen en la propiedad **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).
    
5. Llama a [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) para hacer lo siguiente: 
    
    1. Expanda todas las listas de distribuci�n personal y destinatarios personalizados y reemplace todos los nombres de presentaci�n que ha cambiado con sus nombres originales.
        
    2. Quite los nombres duplicados.
        
    3. Compruebe para cualquier preprocesamiento necesarios y, si es necesario preprocesamiento, establecer la marca NEEDS_PREPROCESSING y la propiedad **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)), que está reservada para MAPI. 
        
    4. Establecer el indicador NEEDS_SPOOLER si el almac�n de mensajes se complementa con un transporte y no puede controlar todos los destinatarios. 
    
6. Si se establece la marca de mensaje NEEDS_PREPROCESSING, realiza las tareas siguientes:
    
    1. Coloca el mensaje en la cola de salida con el bit SUBMITFLAG_PREPROCESS establecido en la propiedad **PR_SUBMIT_FLAGS** . 
        
    2. Notifica a la cola MAPI que ha cambiado la cola.
        
    3. Devuelve el control al cliente y contin�a el flujo de mensajes en la cola MAPI. La cola MAPI realiza las tareas siguientes: 
    
       1. Bloquea el mensaje mediante una llamada a [IMsgStore::SetLockState](imsgstore-setlockstate.md).
            
       2. Lleva a cabo el preprocesamiento necesarias mediante una llamada a todas las funciones de preprocesamiento en el orden de registro. Los proveedores de transporte llame a [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar las funciones de preprocesamiento. 
            
       3. Las llamadas [IMessage::SubmitMessage](imessage-submitmessage.md) en el mensaje abierto para indicar al mensaje almacenar esa preprocesamiento está completa. 
    
Si se ha producido ningún preprocesamiento o hubo preprocesamiento y la cola MAPI llamado **SubmitMessage**, el proveedor de almacén de mensajes hace lo siguiente en el proceso de cliente: 
  
- Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):
    
   - Administra a todos los destinatarios que pueden administrar.
    
   - Establece la propiedad **PR_RESPONSIBILITY** en TRUE para todos los destinatarios que administra. 
    
   - Si todos los destinatarios se conocen en este almac�n de acoplamiento ajustado y transporte, realiza las tareas siguientes: 
    
     - Llama a [IMAPISupport::CompleteMsg](imapisupport-completemsg.md) si el mensaje se preprocesa o el proveedor de almacén de mensajes que desea a la cola MAPI para procesar el mensaje completo. Flujo de mensajes continúa con la cola de MAPI. 
    
     - Si el mensaje no se preprocesa o el proveedor de almacén de mensajes no desea que la cola MAPI para llevar a cabo el procesamiento de mensajes, realiza las tareas siguientes:
    
       1. Copia el mensaje a la carpeta identificado por el identificador de entrada en la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)), si establece.
            
       2. Elimina el mensaje si la propiedad **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) se ha establecido en TRUE.
            
       3. Desbloquea el mensaje si está bloqueada.
            
       4. Devuelve al cliente. Flujo de mensajes está completado.
    
  - Si el mensaje se preprocesa o el proveedor que desea la cola MAPI para llevar a cabo el procesamiento de mensajes, realiza las tareas siguientes:
    
    1. Llama a [IMAPISupport::CompleteMsg](imapisupport-completemsg.md). 
          
    2. Sigue el flujo de mensajes con la cola de MAPI. Para obtener más información, vea [enviar mensajes: tareas de cola de impresión de MAPI](sending-messages-mapi-spooler-tasks.md).
    
  - Si el mensaje no se preprocesa o el proveedor no desea que la cola de impresión para llevar a cabo el procesamiento de mensajes, realiza las tareas siguientes:
    
    1. Copia el mensaje a la carpeta identificada por el identificador de entrada en la propiedad **PR_SENTMAIL_ENTRYID** , si establece. 
        
    2. Elimina el mensaje si la propiedad **PR_DELETE_AFTER_SUBMIT** se ha establecido en TRUE. 
        
    3. Desbloquea el mensaje si está bloqueada. 
        
    4. Devuelve al autor de la llamada. Flujo de mensajes está completado.
    
- Si el almac�n de mensajes no est� estrechamente asociado a un transporte, no todos los destinatarios eran conocidos para el almac�n de mensajes o se establece la marca NEEDS_SPOOLER, realiza las tareas siguientes:
    
  1. Coloca el mensaje en la cola de salida sin establecer el bit SUBMITFLAG_PREPROCESS en la propiedad **PR_SUBMIT_FLAGS**. 
    
  2. Notifica a la cola MAPI que ha cambiado la cola de salida al generar una notificaci�n de la tabla. 
    
  3. Devuelve al cliente y el flujo de mensajes contin�a con un conjunto de tareas que se realizan por la cola MAPI.
    
## <a name="see-also"></a>Vea también

- [Caracter�sticas de almac�n de mensajes](message-store-features.md)

