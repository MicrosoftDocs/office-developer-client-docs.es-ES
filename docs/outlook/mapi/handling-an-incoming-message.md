---
title: Controlar un mensaje entrante
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5705af6c8efaf42ae27d1b39bb28d162971ebf9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816929"
---
# <a name="handling-an-incoming-message"></a>Controlar un mensaje entrante

**Hace referencia a**: Outlook 
  
Un mensaje entrante es un mensaje que se ha enviado a través de uno o varios sistemas de mensajería. Es posible que se han enviado sólo a usted o a muchos otros destinatarios. Los mensajes entrantes se colocan en una carpeta de recepción designada para almacenar los mensajes de una clase determinada. Puede configurar recibir otra carpeta para cada clase de mensaje que administrar o usar una carpeta para todas las clases.
  
Si se ha registrado para notificaciones de correo nuevo con el almacén de mensajes, se le notificará cada vez que un mensaje se coloca en una carpeta de recepción. Si no se ha registrado para notificaciones de correo nuevo, debe abrir el correspondiente recibir carpeta periódicamente para comprobar manualmente la llegada de mensajes nuevos.
  
Los clientes se registre para notificaciones de correo nuevo mediante la configuración de los parámetros a [IMsgStore::Advise](imsgstore-advise.md) como se indica a continuación: 
  
- Establece _cbEntryID_ en 0. 
    
- Establecer _lpEntryID_ en NULL. 
    
- Establezca _ulEventMask_ en fnevNewMail. 
    
El parámetro _lpNotifications_ en la llamada al método **IMAPIAdviseSink::OnNotify** apunta a un **NEWMAIL\_notificación** estructura que contiene información sobre el mensaje entrante, como su clase de mensaje, su entrada identificador, el identificador de entrada de su carpeta principal y el contenido de su propiedad **PR_MESSAGE_FLAGS** . Para obtener más información acerca de cómo registrar para y controlar las notificaciones, vea [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) y [Controlar notificaciones](handling-notifications.md). 
  
Antes de mostrar un mensaje entrante a un usuario, determine si su clase de mensaje es una clase que admite el cliente. En caso contrario, pase por alto el mensaje. Si la clase es uno que admita, puede abrir y mostrar el mensaje con un formulario que sea apropiado para la clase de mensaje del mensaje. La elección de los formularios se basa en la clase de mensaje. Los mensajes que pertenecen a la clase IPM usar un formulario predeterminado que se implementa mediante MAPI. Los mensajes que pertenecen a las clases personalizadas definidas por los clientes pueden usar formularios especializados definidas por el cliente o en el formulario predeterminado MAPI.
  
## <a name="open-and-display-an-incoming-message"></a>Abrir y mostrar un mensaje entrante
  
1. Llame a **IMsgStore::GetReceiveFolder** para recuperar el identificador de entrada de la carpeta de recepción para la clase de mensaje del mensaje y pasar este identificador de entrada a **IMsgStore::OpenEntry** para abrir la carpeta. Para obtener más información, vea [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore::OpenEntry](imsgstore-openentry.md)y [Abrir una carpeta de almacén de mensajes](opening-a-message-store-folder.md).
    
2. Llamar al método **IMAPIContainer::GetContentsTable** de la carpeta de recepción para recuperar su tabla de contenido. Para obtener más información, vea [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). Llamar al método **IMAPITable:: QueryRows** de la tabla para recuperar todas las filas de la tabla. Para obtener más información, vea [IMAPITable:: QueryRows](imapitable-queryrows.md) y [Tablas de contenido](contents-tables.md). Para obtener más información acerca de cómo mostrar una tabla de contenido, vea [Mostrar una tabla de contenido de carpeta](displaying-a-folder-contents-table.md).
    
3. Si su cliente es interactivo, permitir que el usuario seleccione un mensaje en la tabla y determinar el formulario que se usará para mostrar ese mensaje. Los clientes pueden utilizar el formulario predeterminado proporcionado por MAPI o de un formulario personalizado. Para obtener más información, vea [Controlar formularios de MAPI](handling-mapi-forms.md).
    
4. Llame a **IMsgStore::OpenEntry** para abrir el mensaje. Para obtener más información, vea [Abrir un mensaje](opening-a-message.md).
    
5. Procesar el texto del mensaje. Para obtener más información, vea [El texto del mensaje de apertura](opening-message-text.md).
    
6. Representar cada uno de los datos adjuntos de mensajes. Para obtener más información, vea [representación de un dato adjunto en texto sin formato](rendering-an-attachment-in-plain-text.md) o [datos adjuntos en formato RTF texto de representación](rendering-an-attachment-in-rtf-text.md).
    
7. Abrir un archivo adjunto si así lo desea. Para obtener más información, vea [Abrir un archivo adjunto](opening-an-attachment.md).
    
## <a name="in-this-section"></a>En esta sección

- [Texto del mensaje de apertura](opening-message-text.md): describe cómo abrir el texto del mensaje.
    
- [Representación de un dato adjunto en texto sin formato](rendering-an-attachment-in-plain-text.md): describe cómo representar un dato adjunto en texto sin formato.
    
- [Representación de un dato adjunto en texto RTF](rendering-an-attachment-in-rtf-text.md): describe cómo representar un dato adjunto en texto con formato.
    
- [Abrir datos adjuntos](opening-an-attachment.md): se describe cómo abrir un archivo adjunto.
    

