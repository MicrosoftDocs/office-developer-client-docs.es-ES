---
title: Tratamiento de un mensaje saliente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ab293ee3813d77c3a954e8364736a89bc2330feb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816925"
---
# <a name="handling-an-outgoing-message"></a>Tratamiento de un mensaje saliente

**Hace referencia a**: Outlook 
  
Un mensaje saliente es un mensaje que puede enviarse a uno o más destinatarios a través de uno o varios sistemas de mensajería o enviarse a una carpeta en un almacén de mensajes.
  
## <a name="create-and-send-an-outgoing-message"></a>Crear y enviar un mensaje saliente
  
1. Abra el almacén de mensajes predeterminado. Para obtener más información, vea [Abrir un almacén de mensajes](opening-a-message-store.md) y [Abrir el almacén de mensajes predeterminado](opening-the-default-message-store.md).
    
2. Abra la carpeta Bandeja de salida. Para obtener más información, vea [Abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
    
3. Llamar al método **IMAPIFolder::CreateMessage** de la carpeta Bandeja de salida para crear el nuevo mensaje. Para obtener más información, vea [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Crear una lista de destinatarios con uno o más destinatarios resueltos. Para obtener más información, vea [crear una lista de destinatarios](creating-a-recipient-list.md).
    
5. Opcionalmente, agregue a un asunto. Para obtener más información, vea [crear un asunto del mensaje](creating-a-message-subject.md).
    
6. Agregue el texto del mensaje. Para obtener más información, vea [Creación de texto del mensaje](creating-message-text.md).
    
7. Si el texto del mensaje tiene el formato, agregar información de representación. Para obtener más información, vea [Agregar información de representación en texto con formato](adding-rendering-information-to-formatted-text.md).
    
8. De forma opcional, agregue uno o más datos adjuntos. Para obtener más información, vea [crear un datos adjuntos del mensaje](creating-a-message-attachment.md).
    
9. Defina otras propiedades del mensaje como desee y, a continuación, guardar y enviar el mensaje mediante una llamada a **IMessage::SubmitMessage**. Para obtener más información, vea [IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Eliminar el mensaje enviado si la **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) (propiedad) se establece en TRUE o mover a la carpeta identificada por la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). Para obtener más información, consulte [procesamiento de un mensaje enviado](processing-a-sent-message.md).
    
Si desea intermittantly guardar el mensaje antes de enviarlo, llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje. Para obtener más información, vea [Guardar un mensaje](saving-a-message.md) o [Enviar un mensaje](sending-a-message.md). 
  
## <a name="in-this-section"></a>En esta sección

- [Creación de una lista de destinatarios](creating-a-recipient-list.md): describe cómo crear una lista de destinatarios.
    
- [Creación de un asunto del mensaje](creating-a-message-subject.md): se describe cómo crear un asunto opcional para un mensaje.
    
- [Creación de texto del mensaje](creating-message-text.md): se describen los procedimientos para crear el texto del mensaje.
    
- [Adición de información de representación en texto con formato](adding-rendering-information-to-formatted-text.md): describe donde en texto con formato adjuntos se va a procesar.
    
- [Creación de un dato adjunto de mensaje](creating-a-message-attachment.md): se describe cómo crear los datos adjuntos.
    
- [Guardar un mensaje](saving-a-message.md): describe cómo los clientes guardar los mensajes.
    
- [Enviar un mensaje](sending-a-message.md): describe cómo enviar un mensaje.
    
- [Procesamiento de un mensaje enviado](processing-a-sent-message.md): describe cómo se envían los mensajes se pueden procesar.
    

