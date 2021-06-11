---
title: Controlar los mensajes entrantes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f3fbe34793e3520b26b984f4bd6b14fbcab7a951
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438984"
---
# <a name="handling-an-incoming-message"></a>Controlar los mensajes entrantes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un mensaje entrante es un mensaje que se ha enviado a través de uno o varios sistemas de mensajería. Es posible que solo se haya enviado a usted o a muchos otros destinatarios. Los mensajes entrantes se colocan en una carpeta de recepción designada para contener mensajes de una clase determinada. Puede configurar una carpeta de recepción diferente para cada clase de mensaje que controle o use una carpeta para todas las clases.
  
Si se ha registrado para nuevas notificaciones de correo con el almacén de mensajes, se le notificará siempre que se coloque un mensaje en una carpeta de recepción. Si no se ha registrado para nuevas notificaciones de correo, debe abrir la carpeta de recepción adecuada periódicamente para comprobar manualmente la llegada de nuevos mensajes.
  
Los clientes se registran para nuevas notificaciones de correo estableciendo los parámetros en [IMsgStore::Advise](imsgstore-advise.md) de la siguiente manera: 
  
- Establezca  _cbEntryID_ en 0. 
    
- Establezca  _lpEntryID_ en NULL. 
    
- Establezca  _ulEventMask_ en fnevNewMail. 
    
El parámetro _lpNotifications_ de la llamada al método **IMAPIAdviseSink::OnNotify** apunta a una estructura DE NOTIFICACIÓN **NEWMAIL \_** que contiene información sobre el mensaje entrante, como su clase de mensaje, su identificador de entrada, el identificador de entrada de su carpeta primaria y el contenido de su propiedad **PR_MESSAGE_FLAGS.** Para obtener más información acerca del registro y el control de notificaciones, vea [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) y [Handling Notifications](handling-notifications.md). 
  
Antes de mostrar un mensaje entrante a un usuario, determine si su clase de mensaje es una clase compatible con el cliente. Si no es así, ignore el mensaje. Si la clase es compatible, puede abrir y mostrar el mensaje con un formulario adecuado para la clase de mensaje del mensaje. La elección de los formularios se basa en la clase de mensaje. Los mensajes que pertenecen a la clase IPM usan un formulario predeterminado implementado por MAPI. Los mensajes que pertenecen a clases personalizadas definidas por los clientes pueden usar formularios especializados definidos por el cliente o el formulario predeterminado MAPI.
  
## <a name="open-and-display-an-incoming-message"></a>Abrir y mostrar un mensaje entrante
  
1. Llama a **IMsgStore::GetReceiveFolder** para recuperar el identificador de entrada de la carpeta de recepción de la clase de mensaje del mensaje y pasar este identificador de entrada a **IMsgStore::OpenEntry** para abrir la carpeta. Para obtener más información, vea [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore::OpenEntry](imsgstore-openentry.md)y [Opening a Message Store Folder](opening-a-message-store-folder.md).
    
2. Llame al método **IMAPIContainer::GetContentsTable** de la carpeta de recepción para recuperar su tabla de contenido. Para obtener más información, [vea IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). Llame al método **IMAPITable::QueryRows** de la tabla para recuperar todas las filas de la tabla. Para obtener más información, [vea IMAPITable::QueryRows](imapitable-queryrows.md) and [Contents Tables](contents-tables.md). Para obtener más información acerca de cómo mostrar una tabla de contenido, vea [Mostrar una tabla de contenido de carpeta.](displaying-a-folder-contents-table.md)
    
3. Si el cliente es interactivo, permita al usuario seleccionar un mensaje de la tabla y determinar el formulario que se usará para mostrar ese mensaje. Los clientes pueden usar el formulario predeterminado proporcionado por MAPI o un formulario personalizado. Para obtener más información, vea [Handling MAPI Forms](handling-mapi-forms.md).
    
4. Llama **a IMsgStore::OpenEntry** para abrir el mensaje. Para obtener más información, vea [Opening a Message](opening-a-message.md).
    
5. Procesar el texto del mensaje. Para obtener más información, vea [Opening Message Text](opening-message-text.md).
    
6. Represente cada uno de los datos adjuntos del mensaje. Para obtener más información, vea [Rendering an Attachment in Plain Text](rendering-an-attachment-in-plain-text.md) o Rendering an Attachment in RTF [Text](rendering-an-attachment-in-rtf-text.md).
    
7. Abra un archivo adjunto si lo desea. Para obtener más información, [vea Opening an Attachment](opening-an-attachment.md).
    
## <a name="in-this-section"></a>En esta sección

- [Abrir texto del mensaje:](opening-message-text.md)describe cómo abrir el texto del mensaje.
    
- [Representación de datos adjuntos en texto sin](rendering-an-attachment-in-plain-text.md)formato: describe cómo representar datos adjuntos en texto sin formato.
    
- [Representación de datos adjuntos en texto RTF:](rendering-an-attachment-in-rtf-text.md)describe cómo representar datos adjuntos en texto con formato.
    
- [Abrir datos adjuntos:](opening-an-attachment.md)describe cómo abrir datos adjuntos.
    

