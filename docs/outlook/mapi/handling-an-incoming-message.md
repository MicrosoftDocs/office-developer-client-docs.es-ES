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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299408"
---
# <a name="handling-an-incoming-message"></a>Controlar los mensajes entrantes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un mensaje entrante es un mensaje que se ha enviado a través de uno o varios sistemas de mensajería. Puede que se le haya enviado solo a usted o a muchos otros destinatarios. Los mensajes entrantes se colocan en una carpeta de recepción designada para contener mensajes de una clase determinada. Puede configurar una carpeta de recepción diferente para cada clase de mensaje que controle o use una carpeta para todas las clases.
  
Si se ha registrado para recibir notificaciones de correo nuevo con el almacén de mensajes, recibirá una notificación cada vez que se coloque un mensaje en una carpeta de recepción. Si no se ha registrado para recibir notificaciones de correo nuevo, debe abrir la carpeta de recepción correspondiente periódicamente para comprobar de forma manual la llegada de mensajes nuevos.
  
Los clientes se registran para notificaciones de correo nuevo mediante la configuración de los parámetros en [IMsgStore:: Advise](imsgstore-advise.md) de la siguiente manera: 
  
- Establezca _cbEntryID_ en 0. 
    
- Establezca _lpEntryID_ en NULL. 
    
- Establezca _ulEventMask_ en fnevNewMail. 
    
El parámetro _lpNotifications_ en la llamada a su método **IMAPIAdviseSink:: BENOTIFY** apunta a una estructura de **notificación NEWMAIL\_** que contiene información sobre el mensaje entrante, como su clase de mensaje, su entrada identificador, el identificador de entrada de su carpeta principal y el contenido de su propiedad **PR_MESSAGE_FLAGS** . Para obtener más información sobre cómo registrar y controlar las notificaciones, vea [IMAPIAdviseSink::](imapiadvisesink-onnotify.md)NEWMAIL_NOTIFICATION, [](newmail_notification.md) **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) y [controlar](handling-notifications.md)las notificaciones. 
  
Antes de mostrar un mensaje entrante a un usuario, determine si su clase de mensaje es una clase que admite su cliente. Si no es así, ignore el mensaje. Si la clase es una que admite, puede abrir y mostrar el mensaje con un formulario que sea adecuado para la clase de mensaje del mensaje. La elección de los formularios se basa en la clase Message. Los mensajes que pertenecen a la clase IPM usan un formulario predeterminado implementado por MAPI. Los mensajes que pertenecen a las clases personalizadas definidas por los clientes pueden usar formularios especializados definidos por el cliente o el formulario predeterminado de MAPI.
  
## <a name="open-and-display-an-incoming-message"></a>Abrir y mostrar un mensaje entrante
  
1. Llame a **IMsgStore:: GetReceiveFolder** para recuperar el identificador de entrada de la carpeta de recepción para la clase de mensaje del mensaje y pase este identificador de entrada a **IMsgStore:: OpenEntry** para abrir la carpeta. Para obtener más información, vea [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md)y [abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
    
2. Llame al método **IMAPIContainer:: GetContentsTable** de la carpeta de recepción para recuperar su tabla de contenido. Para obtener más información, vea [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md). Llame al método **IMAPITable:: QueryRows** de la tabla para recuperar todas las filas de la tabla. Para obtener más información, consulte [IMAPITable:: QueryRows](imapitable-queryrows.md) y [tablas de contenido](contents-tables.md). Para obtener más información sobre cómo mostrar una tabla de contenido, vea [Mostrar una tabla de contenido de una carpeta](displaying-a-folder-contents-table.md).
    
3. Si el cliente es interactivo, permita al usuario seleccionar un mensaje de la tabla y determinar el formulario que se va a usar para mostrar el mensaje. Los clientes pueden usar el formulario predeterminado proporcionado por MAPI o un formulario personalizado. Para obtener más información, consulte [Handling MAPI Forms](handling-mapi-forms.md).
    
4. Llame a **IMsgStore:: OpenEntry** para abrir el mensaje. Para obtener más información, vea [abrir un mensaje](opening-a-message.md).
    
5. Procesar el texto del mensaje. Para obtener más información, vea [abrir texto de mensaje](opening-message-text.md).
    
6. RePresente cada uno de los datos adjuntos del mensaje. Para obtener más información, vea [representar datos adjuntos en texto sin formato](rendering-an-attachment-in-plain-text.md) o [representar datos adjuntos en texto RTF](rendering-an-attachment-in-rtf-text.md).
    
7. Abra un archivo de datos adjuntos si lo desea. Para obtener más información, consulte [apertura de datos](opening-an-attachment.md)adjuntos.
    
## <a name="in-this-section"></a>En esta sección

- [Texto del mensaje de apertura](opening-message-text.md): describe cómo abrir el texto del mensaje.
    
- [Representar datos adjuntos en texto sin formato](rendering-an-attachment-in-plain-text.md): describe cómo representar datos adjuntos en texto sin formato.
    
- [Representar datos adjuntos en texto RTF](rendering-an-attachment-in-rtf-text.md): describe cómo representar datos adjuntos en texto con formato.
    
- [Apertura de datos](opening-an-attachment.md)adjuntos: describe cómo abrir datos adjuntos.
    

