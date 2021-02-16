---
title: Controlar los mensajes salientes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 07785ac82c41108b4333b3c370e3d2f5bfd1426a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407630"
---
# <a name="handling-an-outgoing-message"></a>Controlar los mensajes salientes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un mensaje saliente es un mensaje que se puede enviar a uno o más destinatarios a través de uno o más sistemas de mensajería o publicarse en una carpeta de un almacén de mensajes.
  
## <a name="create-and-send-an-outgoing-message"></a>Crear y enviar un mensaje saliente
  
1. Abra el almacén de mensajes predeterminado. Para obtener más información, vea [Abrir un almacén de mensajes](opening-a-message-store.md) y Abrir el almacén de mensajes [predeterminado.](opening-the-default-message-store.md)
    
2. Abra la carpeta Bandeja de salida. Para obtener más información, vea [Abrir una carpeta de almacén de mensajes.](opening-a-message-store-folder.md)
    
3. Llame al método **IMAPIFolder::CreateMessage** de la carpeta Bandeja de salida para crear el nuevo mensaje. Para obtener más información, [vea IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Cree una lista de destinatarios con uno o más destinatarios resueltos. Para obtener más información, vea [Crear una lista de destinatarios.](creating-a-recipient-list.md)
    
5. Opcionalmente, agregue un asunto. Para obtener más información, vea [Crear un asunto del mensaje.](creating-a-message-subject.md)
    
6. Agregue el texto del mensaje. Para obtener más información, vea [Crear texto de mensaje.](creating-message-text.md)
    
7. Si el texto del mensaje tiene formato, agregue información de representación. Para obtener más información, vea [Agregar información de representación al texto con formato.](adding-rendering-information-to-formatted-text.md)
    
8. Opcionalmente, agregue uno o más datos adjuntos. Para obtener más información, vea [Creación de datos adjuntos de un mensaje.](creating-a-message-attachment.md)
    
9. Establezca otras propiedades del mensaje como desee y, a continuación, guarde y envíe el mensaje llamando a **IMessage::SubmitMessage**. Para obtener más información, [vea IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Elimine el mensaje enviado si la propiedad **PR \_ DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) está establecida en TRUE o muévela a la carpeta identificada por la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). Para obtener más información, vea [Procesamiento de un mensaje enviado.](processing-a-sent-message.md)
    
Si desea guardar el mensaje de forma intermitente antes de enviarlo, llame al método [IMAPIProp::SaveChanges del](imapiprop-savechanges.md) mensaje. Para obtener más información, vea Guardar [un mensaje](saving-a-message.md) o Enviar [un mensaje.](sending-a-message.md) 
  
## <a name="in-this-section"></a>En esta sección

- [Creación de una lista de destinatarios:](creating-a-recipient-list.md)describe cómo crear una lista de destinatarios.
    
- [Creación de un asunto de](creating-a-message-subject.md)mensaje: describe cómo crear un asunto opcional para un mensaje.
    
- [Creación de texto de](creating-message-text.md)mensaje: describe cómo crear texto del mensaje.
    
- [Agregar información de representación al texto con](adding-rendering-information-to-formatted-text.md)formato: describe dónde se representarán los datos adjuntos en el texto con formato.
    
- [Creación de datos adjuntos de](creating-a-message-attachment.md)mensajes: describe cómo crear datos adjuntos.
    
- [Guardar un mensaje:](saving-a-message.md)describe cómo los clientes guardarán los mensajes.
    
- [Enviar un mensaje:](sending-a-message.md)describe cómo enviar un mensaje.
    
- [Procesamiento de un mensaje enviado:](processing-a-sent-message.md)describe cómo se pueden procesar los mensajes enviados.
    

