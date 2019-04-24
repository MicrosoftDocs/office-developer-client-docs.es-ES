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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342808"
---
# <a name="handling-an-outgoing-message"></a>Controlar los mensajes salientes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un mensaje saliente es un mensaje que se puede enviar a uno o más destinatarios en uno o varios sistemas de mensajería o se puede exponer en una carpeta de un almacén de mensajes.
  
## <a name="create-and-send-an-outgoing-message"></a>Crear y enviar un mensaje saliente
  
1. Abra el almacén de mensajes predeterminado. Para obtener más información, vea [abrir un almacén de mensajes](opening-a-message-store.md) y [abrir el almacén de mensajes predeterminado](opening-the-default-message-store.md).
    
2. Abra la carpeta Bandeja de salida. Para obtener más información, consulte [abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
    
3. Llame al método **IMAPIFolder:: CreateMessage** de la carpeta Bandeja de salida para crear el nuevo mensaje. Para obtener más información, vea [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md),
    
4. Cree una lista de destinatarios con uno o más destinatarios resueltos. Para obtener más información, vea [crear una lista de destinatarios](creating-a-recipient-list.md).
    
5. Opcionalmente, agregue un asunto. Para obtener más información, vea [crear un asunto de mensaje](creating-a-message-subject.md).
    
6. Agregue el texto del mensaje. Para obtener más información, vea [crear texto de mensaje](creating-message-text.md).
    
7. Si el texto del mensaje tiene formato, agregue información de representación. Para obtener más información, vea [Agregar información de representación al texto con formato](adding-rendering-information-to-formatted-text.md).
    
8. Si lo desea, puede agregar uno o más datos adjuntos. Para obtener más información, vea [crear datos adjuntos de un mensaje](creating-a-message-attachment.md).
    
9. Establezca otras propiedades del mensaje como desee y, a continuación, guarde y envíe el mensaje llamando a **IMessage:: SubmitMessage**. Para obtener más información, vea [IMessage:: SubmitMessage](imessage-submitmessage.md).
    
10. Elimine el mensaje enviado si **la\_propiedad PR DELETE_AFTER_SUBMIT** ([PIDTAGDELETEAFTERSUBMIT](pidtagdeleteaftersubmit-canonical-property.md)) está establecida en true o muévala a la carpeta identificada por la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). Para obtener más información, consulte [procesar un mensaje enviado](processing-a-sent-message.md).
    
Si desea intermittantly guardar el mensaje antes de enviarlo, llame al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del mensaje. Para obtener más información, vea, [guardar un mensaje](saving-a-message.md) o [Enviar un mensaje](sending-a-message.md). 
  
## <a name="in-this-section"></a>En esta sección

- [Creación de una lista](creating-a-recipient-list.md)de destinatarios: describe cómo crear una lista de destinatarios.
    
- [Creación de un asunto de mensaje](creating-a-message-subject.md): describe cómo crear un asunto opcional para un mensaje.
    
- [Creación de texto de mensaje](creating-message-text.md): describe cómo crear texto de mensaje.
    
- [Agregar información de representación a texto con formato](adding-rendering-information-to-formatted-text.md): describe en qué lugar del texto con formato se va a representar un dato adjunto.
    
- [Creación de datos adjuntos de un mensaje](creating-a-message-attachment.md): describe cómo crear datos adjuntos.
    
- [Guardar un mensaje](saving-a-message.md): describe cómo los clientes guardan los mensajes.
    
- [Enviar un mensaje](sending-a-message.md): describe cómo enviar un mensaje.
    
- [Procesar un mensaje enviado](processing-a-sent-message.md): describe cómo se pueden procesar los mensajes enviados.
    

