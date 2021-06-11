---
title: Guardar un mensaje en la Bandeja de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407896"
---
# <a name="saving-a-message-in-the-inbox"></a>Guardar un mensaje en la Bandeja de entrada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para almacenar un mensaje en la Bandeja de entrada sin destinatarios**
  
1. Llame [a IMsgStore::GetReceiveFolder para](imsgstore-getreceivefolder.md) recuperar el identificador de entrada de la Bandeja de entrada. 
    
2. Llama [a IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir la Bandeja de entrada y recuperar un puntero. 
    
3. Llama al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) de la Bandeja de entrada para crear el mensaje. 
    
4. Llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) del mensaje para agregar las propiedades **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) y **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)). 
    
5. Cree cada dato adjunto, establezca sus propiedades y guárdelo. Para obtener información detallada acerca de cómo agregar datos adjuntos a los mensajes, vea [Creating a Message Attachment](creating-a-message-attachment.md).
    
6. Llama **a IMessage::SaveChanges** para guardar el mensaje. En este momento aparecerá en la tabla de contenido de la Bandeja de entrada. 
    
Si desea guardar un mensaje de forma intermitente antes de que aparezca en la tabla de contenido de la Bandeja de entrada, creelo en su lugar en una carpeta oculta, como la carpeta raíz del subárbol IPM y, a continuación, muévelo a la Bandeja de entrada. 
  

