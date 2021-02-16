---
title: Publicar un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc3e1546-e58b-413f-82d7-4efeb86b0000
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2c174d48a19e23de725e1d5a1533130175f2ab00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429771"
---
# <a name="posting-a-message"></a>Publicar un mensaje

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Publicar un mensaje es similar al envío de un mensaje. La principal diferencia es el destino. En lugar de dirigirse a uno o más destinatarios en uno o más sistemas de mensajería, un mensaje publicado permanece en una carpeta del almacén de mensajes actual.
  
### <a name="to-post-a-message"></a>Para publicar un mensaje
  
1. Abra la carpeta de destino llamando a [IMsgStore::OpenEntry](imsgstore-openentry.md). Si la carpeta de destino es la Bandeja de entrada, busque el identificador de entrada que se va a pasar **a OpenEntry** llamando a [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
2. Llame [a IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para crear el mensaje. 
    
3. Llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) del mensaje para establecer: 
    
   - Marca MSGFLAG_READ en la **propiedad PidTagMessageFlags** ( [PR_MESSAGE_FLAGS](pidtagmessageflags-canonical-property.md)).
    
   - El **PR_SENDER** propiedades. 
    
   - El **PR_SENT_REPRESENTING** propiedades. 
    
   - Propiedad **PR_RECEIPT_TIME** ([PidTagReceiptTime](pidtagreceipttime-canonical-property.md)).
    
   - La **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).
    
   - Propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
    
   - Propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).
    
   - Cualquier propiedad requerida por la clase de mensaje.
    
4. Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje para guardar el mensaje. 
    
5. Si es necesario, cree un archivo adjunto, establezca sus propiedades y guárdelo. Para obtener más información acerca de cómo agregar datos adjuntos a los mensajes, vea [Creación de datos adjuntos de un mensaje.](creating-a-message-attachment.md)
    
6. Llame **a IMessage::SaveChanges** para guardar el mensaje. En este momento aparecerá en la tabla de contenido de la carpeta de destino. 
    
Tenga en cuenta que no crea una lista de destinatarios. En su lugar, se establecen varias propiedades que normalmente establece un proveedor de transporte para un mensaje enviado. 
  
Si desea guardar un mensaje de forma intermitente antes de que aparezca en la tabla de contenido de la carpeta visible, cráigalo en su lugar en una carpeta oculta, como la carpeta raíz del subárbol IPM y, a continuación, muévelo a la carpeta de destino. 
  

