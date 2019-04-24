---
title: Creación de una lista de destinatarios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332910"
---
# <a name="creating-a-recipient-list"></a>Creación de una lista de destinatarios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una lista de destinatarios es una estructura [ADRLIST](adrlist.md) que contiene una matriz de estructuras de valores de propiedad para cada destinatario de mensaje: destino del mensaje. Un destinatario puede representar un usuario humano, un equipo o una carpeta. Todos los mensajes que se van a enviar requieren al menos un destinatario que ha recibido el proceso de resolución de nombres, es decir **** , un proceso para asegurarse de que la propiedad de ([PidTagEntryId](pidtagentryid-canonical-property.md)) se incluye en la matriz de valores de propiedad del destinatario. 
  
Las propiedades de un destinatario son una combinación de propiedades de la libreta de direcciones y propiedades del mensaje. Las propiedades de los destinatarios se pueden aplicar a todos los mensajes de un destinatario en particular o solo al mensaje actual. Tanto el almacén de mensajes como los proveedores de transporte pueden establecer las propiedades de los destinatarios. 
  
Cada destinatario debe tener un conjunto principal de propiedades en su matriz de valores de propiedad en el momento en que el mensaje esté listo para enviarse. El conjunto necesario de propiedades de destinatarios incluye:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
Estas propiedades se usan para tener acceso al destinatario, enviarle mensajes y compararlo con otros usuarios. No todas estas propiedades deben estar disponibles de inmediato. Puede Agregar un destinatario inicialmente sin conocer su identificador de entrada, sino que depende del proceso de resolución de nombres para asignar esta propiedad. En algún momento antes de enviar un mensaje, llame a [IAddrBook:: ResolveName](iaddrbook-resolvename.md) para asegurarse de que se resuelven todos los destinatarios de la lista de destinatarios. Para obtener más información, vea [resolver un nombre de destinatario](resolving-a-recipient-name.md).
  
Las listas de destinatarios se pueden crear a partir de usuarios de mensajería o entradas de listas de distribución en un contenedor de libretas de direcciones o de desventajas. Las cancelaciones son destinatarios que se crean como entradas temporales para usarse solo para enviar un solo mensaje o como entradas que se agregarán a la libreta personal de direcciones. MAPI define el formato de una dirección y un identificador de entrada de un solo uso. Para obtener más información sobre estos formatos, vea [direcciones de un solo uso](one-off-addresses.md) y [identificadores de entrada de un solo uso](one-off-entry-identifiers.md).
  
Puede permitir que los usuarios creen sus listas de destinatarios:
  
- Solo con entradas de la libreta de direcciones.
    
- Solo con las entradas de uso único.
    
- Con una combinación de destinatarios de la libreta de direcciones y una sola desventajas.
    
 **Para crear una lista de destinatarios mediante el cuadro de diálogo Dirección común**
  
1. Asigne una estructura [ADRPARM](adrparm.md) y un puntero a una estructura [ADRLIST](adrlist.md) . 
    
2. Cero la memoria de la estructura **ADRPARM** y el puntero **ADRLIST** se establece en NULL. 
    
3. Llame a [IAddrBook:: Address](iaddrbook-address.md) para mostrar el cuadro de diálogo address y rellenar la estructura **ADRPARM** . 
    
4. Llame a [IMessage:: ModifyRecipients](imessage-modifyrecipients.md), pasando el puntero **ADRLIST** . Esta estructura contendrá las propiedades de cada uno de los destinatarios seleccionados por el usuario. 
    
 **Para crear una lista de destinatarios mediante programación**
  
1. Asigne una estructura **ADRLIST** que contenga una estructura [ADRENTRY](adrentry.md) para cada uno de los destinatarios que se incluirán en la lista. Haga que cada estructura **ADRENTRY** sea lo suficientemente grande como para guardar cada una de las propiedades y **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) necesarias.
    
2. Para cada destinatario, establezca la matriz de valores de propiedad para su miembro **aEntries** en la estructura **ADRLIST** . 
    
3. Llame a [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) con la marca MODRECIP_ADD establecida. 
    

