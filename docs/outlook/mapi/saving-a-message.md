---
title: Guardar un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97bff16b-dc7c-4eed-8834-d0c076d83ca3
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: e61a72691309b2ac632b764c0607f5b1e36b291b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820554"
---
# <a name="saving-a-message"></a>Guardar un mensaje

  
  
**Se aplica a**: Outlook 
  
Antes de que se guarde un mensaje, los clientes normalmente llaman al método [IMAPIProp::SetProps](imapiprop-setprops.md) del mensaje para establecer algunas propiedades además de las propiedades de texto del mensaje, las propiedades de los datos adjuntos, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) y las propiedades asociada con la lista de destinatarios.
  
Establezca la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) en una cadena de caracteres como IPM. Tenga en cuenta que describe la clase del mensaje saliente. Aunque los clientes deben establecer **PR_MESSAGE_CLASS** en todos los mensajes salientes, un valor predeterminado es proporcionado por el proveedor de almacenamiento de mensaje si no se establece. La clase de mensaje predeterminada para los mensajes salientes es IPM. 
  
Establecer la marca MSGFLAG_UNSENT en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Si lo desea, también establecer los indicadores MSGFLAG_READ y MSGFLAG_UNMODIFIED. Configuración de la MSGFLAG_UNMODIFIED permite un mensaje que esté redactando simular un mensaje entregado. Sólo se puede establecer MSGFLAG_UNMODIFIED por los clientes antes de que un mensaje se ha guardado por primera vez. 
  
Cuando esté listo para realizar una copia de un mensaje no enviado permanente, llame a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) en el mensaje y todos sus datos adjuntos. Si va a enviar el mensaje inmediatamente, no es necesario llamar a **SaveChanges**. La llamada a **SubmitMessage** internamente guarda el mensaje como parte de su procesamiento. 
  
Al llamar al método **SaveChanges**, es una buena idea para especificar la marca KEEP_OPEN_READWRITE, que permite que el mensaje que desea modificar en un momento posterior. Otros marcadores configurables incluyen FORCE_SAVE, lo que indica que el mensaje o adjunto debe cerrarse después de que los cambios se confirman, KEEP_OPEN_READONLY, que indica que no se va a realizar ningún cambio adicional, y el indicador para permitir que al proveedor de almacenamiento de mensajes a solicitudes de cliente de proceso por lotes, MAPI_DEFERRED_ERRORS.
  
Es esencial llamar **SaveChanges** por cada dato adjunto en el mensaje antes de llamar a **SaveChanges** para el mensaje. Si no puede guardar un archivo adjunto, los datos adjuntos no se incluirán con el mensaje cuando se envía y no aparecerá en la tabla de datos adjuntos del mensaje. Si no puede guardar el mensaje después de guardar todos los datos adjuntos, se perderá el mensaje y los datos adjuntos. 
  
Cuando se llama a **SaveChanges** , el proveedor de almacenamiento de mensaje actualiza las propiedades siguientes: 
  
- **PR_DISPLAY_TO de MAPI** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) se enumeran a todos los destinatarios principales.
    
- **PR_DISPLAY_TO de MAPI** se enumeran a todos los destinatarios en copia oculta. 
    
- **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) se enumeran a todos los destinatarios en copia oculta.
    
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** establece MSGFLAG_HASATTACH si uno o más datos adjuntos se han guardado y borra MSGFLAG_UNMODIFIED para mostrar que el mensaje ha cambiado. 
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) contiene el tamaño del mensaje más reciente.
    
- **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) proporciona acceso a la tabla de datos adjuntos.
    
- **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) proporciona acceso a la tabla de destinatarios.
    
Algunas propiedades del mensaje normalmente suministradas por los clientes o proveedores de servicio cuando se crea un mensaje. Si un cliente no establecerlos, es hasta el proveedor de almacenamiento de mensajes para actualizarlos en el momento en que se llama a **SaveChanges** . Por ejemplo, si un mensaje de la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) y las propiedades de **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) se establecieron cuando se creó el mensaje, no es necesario modificar en el momento de guardar. Sin embargo, los proveedores de almacén de mensajes que olvidó establecerlas durante la creación del mensaje deben establecerlas la primera vez que se llama a **SaveChanges** . 
  
Si el **valor de SaveChanges** devuelve MAPI_E_CORRUPT_DATA, suponga que los datos que se guardan están ahora perdido. Los proveedores de almacén de mensajes que usan un modelo de servidor de cliente para su implementación podrían devolver este valor cuando se pierde la conexión de red o el servidor no se está ejecutando. Antes de devolver un error al usuario, intente escribir y guardar los datos de una segunda vez mediante una llamada a **SetProps** seguida de otra llamada a **SaveChanges**. Si los datos se almacena en caché localmente, esto no debería ser un problema. Sin embargo, si no hay ninguna caché local o se produce un error en la segunda llamada **SaveChanges** , mostrar un error para alertar al usuario sobre el problema. 
  

