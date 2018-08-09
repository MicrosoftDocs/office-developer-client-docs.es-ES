---
title: Crear una lista de destinatarios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fa23377a8b080ae9dac3e31dfa137ca03a242c74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816632"
---
# <a name="creating-a-recipient-list"></a>Crear una lista de destinatarios

  
  
**Hace referencia a**: Outlook 
  
Una lista de destinatarios es una estructura [ADRLIST](adrlist.md) que contiene una matriz de estructuras de valor de propiedad para cada destinatario de mensaje: destino para el mensaje. Un destinatario puede representar un usuario humano, un equipo o una carpeta. Todos los mensajes que se envíen requieren al menos un destinatario que ha sido a través del proceso de resolución de nombre: un proceso para asegurarse de que la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) se incluye en la matriz de valores de propiedad del destinatario. 
  
Las propiedades de un destinatario son una combinación de las propiedades de la libreta de direcciones y propiedades del mensaje. Propiedades del destinatario se pueden aplicar a todos los mensajes de un destinatario determinado o solo para el mensaje actual. Ambos almacén de mensajes y los proveedores de transporte pueden establecer las propiedades de destinatarios. 
  
Cada destinatario debe tener un conjunto básico de propiedades en su matriz de valores de propiedad en el momento en que el mensaje está listo para ser enviado. El conjunto de propiedades del destinatario requerido incluyen:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
Estas propiedades se usan para tener acceso a los destinatarios, enviar mensajes a ella y para comparar a otras personas. No todas estas propiedades deben estar disponibles inmediatamente. Puede agregar a un destinatario inicialmente sin necesidad de conocer su identificador de entrada, confiar en el proceso de resolución de nombres para asignar esta propiedad. En algún momento antes de enviar un mensaje, llame a [IAddrBook::ResolveName](iaddrbook-resolvename.md) para asegurarse de que se resuelvan todos los destinatarios en la lista de destinatarios. Para obtener más información, vea la [resolución de un nombre del destinatario](resolving-a-recipient-name.md).
  
Las listas de destinatarios se pueden crear de mensajería a los usuarios o las entradas de la lista de distribución en un contenedor de la libreta de direcciones o de uso único. Uso único es los destinatarios que se crean como entradas temporales para usarse sólo para hacer frente a un solo mensaje o como entradas que se agregarán a una libreta de direcciones personales. El formato de un identificador de entrada con definición y una dirección se define mediante MAPI. Para obtener más información acerca de estos formatos, consulte [Direcciones de uso único](one-off-addresses.md) y los [Identificadores de entrada de uso único](one-off-entry-identifiers.md).
  
Puede habilitar a los usuarios crear sus listas de destinatarios:
  
- Sólo con las entradas de la libreta de direcciones.
    
- Sólo con las entradas de uso único.
    
- Con una combinación de los destinatarios de la libreta de direcciones y de uso único.
    
 **Para crear una lista de destinatarios mediante el cuadro de diálogo dirección comunes**
  
1. Asignar una estructura [ADRPARM](adrparm.md) y un puntero a una estructura [ADRLIST](adrlist.md) . 
    
2. La memoria de la estructura de **ADRPARM** de cero y establecer el puntero **ADRLIST** en NULL. 
    
3. Llame a [IAddrBook::Address](iaddrbook-address.md) para mostrar el cuadro de diálogo dirección y rellenar la estructura **ADRPARM** . 
    
4. Llame a [IMessage::ModifyRecipients](imessage-modifyrecipients.md), pasando el puntero **ADRLIST** . Esta estructura contiene las propiedades de cada uno de los destinatarios seleccionados por el usuario. 
    
 **Para crear una lista de destinatarios mediante programación**
  
1. Asignar una estructura **ADRLIST** que contiene una estructura [ADRENTRY](adrentry.md) para cada uno de los destinatarios que se deben incluir en la lista. Hacer que cada estructura **ADRENTRY** suficientemente grande para contener cada una de las propiedades necesarias y **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).
    
2. Para cada destinatario, establezca la matriz de valores de propiedad para su miembro **aEntries** de la estructura **ADRLIST** . 
    
3. Llame al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) con el conjunto de marca MODRECIP_ADD. 
    

