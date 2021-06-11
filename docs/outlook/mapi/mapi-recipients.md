---
title: Destinatarios MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 88a4360d-6ab8-466e-8ebd-af80227ee00a
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: ebdaf47b4f20763574ffac73bddeb3eb4eeb95df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423695"
---
# <a name="mapi-recipients"></a>Destinatarios MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Every message to be transmitted has one or more recipients, or a set of properties that describe where the message is to be delivered. Because recipients are used only in the context of a message, they are considered subobjects of a message instead of separate MAPI objects. Clients and providers work with recipients using the **IMessage** interface. For more information, see [IMessage: IMAPIProp](imessageimapiprop.md).
  
Los clientes de tener acceso a los destinatarios de un mensaje a trav�s de su tabla de destinatarios. Cada mensaje tiene una tabla de destinatarios que contiene informaci�n resumida sobre cada uno de sus destinatarios. Las columnas que se incluyen en la tabla dependen del estado del mensaje. Cuando est� redactando un mensaje, los destinatarios pueden tener solo tres columnas en la tabla:
  
- Nombre para mostrar o **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- Tipo de destinatario o **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- Identificador de fila o **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Después de que el mensaje haya pasado por el proceso de resolución de nombres, cada destinatario también tendrá un identificador de entrada o una columna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Y cuando se ha enviado el mensaje, las filas de la tabla de destinatarios agregar� dos columnas m�s:
  
- Tipo de dirección o **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- Responsabilidad de transporte o **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Clients can retrieve a message's recipient table by calling its **IMessage::GetRecipientTable** method or its **IMAPIProp::OpenProperty** method. For more information, see [IMessage::GetRecipientTable](imessage-getrecipienttable.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Message store providers are expected to support both of these approaches. The **OpenProperty** approach requires that the client specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_RECIPIENTS** as the property tag. **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) es una propiedad de objeto table que representa la tabla de destinatarios de un mensaje. Message store providers are required to set **PR_MESSAGE_RECIPIENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
For more information about how to work with a recipient table, see [Tablas de destinatarios](recipient-tables.md).
  
Adem�s de que se usa para tener acceso a una tabla de destinatario, se pueden usar **PR_MESSAGE_RECIPIENTS**: 
  
- With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include recipients when copying. For more information see, [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).
    
- En una restricci�n de subobjetos para indicar que la seg�n el elemento secundario se aplique a los destinatarios.
    
Los clientes pueden agregar a destinatarios a un mensaje mediante la copia de las entradas de la libreta de direcciones MAPI o mediante la creaci�n de nuevas entradas. Estas nuevas entradas, denominadas uso �nico, pueden existir temporalmente o guardarse permanentemente en un contenedor modificable. Mientras que los destinatarios que se toman de la libreta de direcciones tienen identificadores de entrada asociados con su proveedor de libreta de direcciones, los destinatarios tienen identificadores de entrada que se ha dado formato mediante MAPI. Transporte proveedores y los identificadores de entrada �nico asociar de clientes con diversos tipos de direcciones. 
  
**IMAPISupport::CreateOneOff** para crear un identificador de entrada �nico para una direcci�n en una salida de llamadas de los proveedores de transporte de mensajes cuando: 
  
- La direcci�n pertenece a una puerta de enlace.
    
- No se puede controlar la direcci�n por un proveedor de libreta de direcciones en el perfil actual.
    
For more information, see [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Los clientes llaman a **IAddrBook::CreateOneOff** para crear un identificador de entrada �nico para una direcci�n en un entrante aparece un mensaje cuando: 
  
- La direcci�n tiene el formato de una direcci�n de uso �nico.
    
- La direcci�n tiene el formato de una direcci�n de Internet.
    
For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).
  
For more information about one-off entry identifiers and addresses, see [Identificadores de entrada �nico](one-off-entry-identifiers.md) and [Direcciones de uso �nico](one-off-addresses.md).
  
Las propiedades de un destinatario son una combinaci�n de propiedades de la libreta de direcciones y propiedades espec�ficas de los destinatarios. Todos los destinatarios tienen las propiedades de la direcci�n base, asignadas por los proveedores de libreta de direcciones. Cuando se usa una entrada como un destinatario de un mensaje saliente, se copian las propiedades de la direcci�n base en la estructura **ADRLIST** que contiene las propiedades de todos los destinatarios de un mensaje. 
  
Dos propiedades que se establecen espec�ficamente para los destinatarios son **PR_RECIPIENT_TYPE** y **PR_RESPONSIBILITY**. **PR_RECIPIENT_TYPE** indica si un destinatario es un destinatario de reenv�o, copia, copia oculta o principal. Los primeros tres tipos se asignan a los destinatarios en los mensajes que se env�an por primera vez. 
  
Si un destinatario no recibe el mensaje y se realiza un intento para enviarlo, el destinatario se copia y se establece su tipo en MAPI_P1 para indicar que se trata de un destinatario de reenv�o. Si s�lo algunos de los destinatarios reciben un mensaje, sus propiedades **PR_RECIPIENT_TYPE** se marcan con la incorporaci�n de la marca MAPI_SUBMITTED cuando se vuelve a enviar el mensaje. Los clientes son necesarios para administrar a destinatarios principales, o los destinatarios con sus **PR_RECIPIENT_TYPE** establecido en MAPI_TO. Todos los dem�s tipos son opcionales. 
  
 **PR_RESPONSIBILITY** se establece para indicar que el proveedor de transporte o no deben administrar Enviar al destinatario. Cuando un mensaje saliente se env�a primero, todos los destinatarios establece **PR_RESPONSIBILITY** en FALSE. Como un proveedor de transporte responsable de enviar a uno o varios de los destinatarios de notificaciones, sus propiedades **PR_RESPONSIBILITY** est�n establecidas en TRUE. 
  

