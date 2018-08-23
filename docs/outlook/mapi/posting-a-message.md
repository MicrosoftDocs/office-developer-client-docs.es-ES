---
title: Enviar un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 61e1039a89f47fe29f9b5a1ba9203cfc88d9797e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577523"
---
# <a name="posting-a-message"></a>Enviar un mensaje

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Enviar un mensaje es similar a enviar un mensaje. La diferencia principal es el destino. En lugar de que se dirige a uno o más destinatarios a través de uno o varios sistemas de mensajería, un mensaje expuesto permanece en una carpeta en el almacén de mensajes actual.
  
### <a name="to-post-a-message"></a>Para publicar un mensaje
  
1. Abra la carpeta de destino mediante una llamada a [IMsgStore::OpenEntry](imsgstore-openentry.md). Si la carpeta de destino es la Bandeja de entrada, busque el identificador de entrada que se pase a **OpenEntry** mediante una llamada a [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
2. Llame a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para crear el mensaje. 
    
3. Llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) del mensaje para establecer: 
    
   - El indicador MSGFLAG_READ en la propiedad **PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).
    
   - Las propiedades **PR_SENDER** . 
    
   - Las propiedades **PR_SENT_REPRESENTING** . 
    
   - La propiedad **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).
    
   - El **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o la propiedad de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).
    
   - La propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
    
   - La propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
   - Las propiedades requeridas por la clase de mensaje.
    
4. Llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje para guardar el mensaje. 
    
5. Si es necesario, cree un archivo adjunto, establezca sus propiedades y vuelva a guardarla. Para obtener más información acerca de cómo agregar datos adjuntos a los mensajes, vea [crear un datos adjuntos del mensaje](creating-a-message-attachment.md).
    
6. Llame a **IMessage::SaveChanges** para guardar el mensaje. En este momento aparecerá en la tabla de contenido de la carpeta de destino. 
    
Tenga en cuenta que no se crea una lista de destinatarios. En su lugar, establecer varias propiedades que se establecen normalmente por un proveedor de transporte de un mensaje enviado. 
  
Si desea guardar un mensaje de forma intermitente antes de que se muestran en la tabla de contenido de la carpeta visible, créelo en su lugar en una carpeta oculta, como la carpeta raíz del subárbol IPM y, a continuación, moverlo a la carpeta de destino. 
  

