---
title: Guardar un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d5ceeb46bded101700aec696a17d690bde80ce6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420936"
---
# <a name="saving-a-message"></a>Guardar un mensaje

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Antes de que se guarde un mensaje, los clientes suelen llamar al método [IMAPIProp:: SetProps](imapiprop-setprops.md) del mensaje para establecer algunas propiedades además de las propiedades de texto del mensaje, propiedades de datos adjuntos, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) y propiedades. asociado a la lista de destinatarios.
  
Establezca la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) en una cadena de caracteres como IPM. Tenga en cuenta que describe la clase del mensaje saliente. Aunque los clientes deben establecer **PR_MESSAGE_CLASS** en todos los mensajes salientes, el proveedor de almacenamiento de mensajes proporciona un valor predeterminado si no lo configura. La clase de mensaje predeterminada para los mensajes salientes es IPM. 
  
Establezca la marca MSGFLAG_UNSENT en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Si lo desea, establezca también las marcas MSGFLAG_READ y MSGFLAG_UNMODIFIED. La configuración de la MSGFLAG_UNMODIFIED permite que un mensaje en composición simule un mensaje entregado. MSGFLAG_UNMODIFIED solo pueden establecerlo los clientes antes de que se guarde un mensaje por primera vez. 
  
Cuando esté listo para realizar una copia permanente de un mensaje no enviado, llame a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) en el mensaje y todos sus datos adjuntos. Si va a enviar el mensaje inmediatamente, no necesita llamar a **SaveChanges**. La llamada a **SubmitMessage** guarda internamente el mensaje como parte de su procesamiento. 
  
Cuando se llama a **SaveChanges**, es una buena idea especificar la marca KEEP_OPEN_READWRITE, que permite modificar el mensaje en un momento posterior. Otros indicadores que se pueden establecer incluyen FORCE_SAVE, que indica que el mensaje o los datos adjuntos deben cerrarse después de confirmar los cambios, KEEP_OPEN_READONLY, que indica que no se realizarán más cambios y la marca para permitir que el proveedor de almacén de mensajes solicitudes de cliente por lotes, MAPI_DEFERRED_ERRORS.
  
Es esencial que llame a **SaveChanges** para todos los datos adjuntos del mensaje antes de llamar a **SaveChanges** para el mensaje. Si no guarda datos adjuntos, los datos adjuntos no se incluirán en el mensaje cuando se envíen y no aparecerán en la tabla de datos adjuntos del mensaje. Si no puede guardar el mensaje después de guardar todos los datos adjuntos, se perderán el mensaje y los datos adjuntos. 
  
Cuando se llama a **SaveChanges** , el proveedor de almacenamiento de mensajes actualiza las siguientes propiedades: 
  
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) enumera todos los destinatarios principales.
    
- **PR_DISPLAY_TO** enumera todos los destinatarios de copia carbón. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) enumera todos los destinatarios ocultos de copia carbón.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** establece MSGFLAG_HASATTACH si se han guardado uno o más datos adjuntos y borra MSGFLAG_UNMODIFIED para mostrar que el mensaje ha cambiado. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) contiene el tamaño más actual del mensaje.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) proporciona acceso a la tabla de datos adjuntos.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) proporciona acceso a la tabla de destinatarios.
    
Algunas propiedades de mensajes suelen suministrarlas los clientes o los proveedores de servicios cuando se crea un mensaje. Si un cliente no los configura, el proveedor de almacén de mensajes debe actualizarlos en el momento en el que se llama a **SaveChanges** . Por ejemplo, si se establecieron las **** propiedades del usuario ([PidTagEntryId](pidtagentryid-canonical-property.md)) y del **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) de un mensaje cuando se creó el mensaje, no es necesario modificarlos en el momento de guardarlo. Sin embargo, los proveedores de almacenamiento de mensajes que no deben establecerse en la creación de mensajes deben establecerlos la primera vez que se llama a **SaveChanges** . 
  
Si **SaveChanges** devuelve MAPI_E_CORRUPT_DATA, asuma que los datos que se están guardando se han perdido. Los proveedores de almacenamiento de mensajes que usan un modelo de cliente-servidor para su implementación pueden devolver este valor cuando se pierde una conexión de red o el servidor no se está ejecutando. Antes de devolver un error al usuario, intente escribir y guardar los datos por segunda vez realizando una llamada a **SetProps** seguida de otra llamada a **SaveChanges**. Si los datos se almacenan en la memoria caché local, esto no debería ser un problema. Sin embargo, si no hay memoria caché local o no se puede realizar la segunda llamada a **SaveChanges** , muestre un error para avisar al usuario del problema. 
  

