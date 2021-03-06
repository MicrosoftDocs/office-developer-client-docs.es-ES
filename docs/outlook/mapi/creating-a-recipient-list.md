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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428217"
---
# <a name="creating-a-recipient-list"></a>Creación de una lista de destinatarios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una lista de destinatarios es una [estructura ADRLIST](adrlist.md) que contiene una matriz de estructuras de valores de propiedad para cada destinatario de mensaje: destino del mensaje. Un destinatario puede representar un usuario humano, una máquina o una carpeta. Todos los mensajes que se enviarán requieren al menos un destinatario que haya pasado por el proceso de resolución de nombres, un proceso para garantizar que la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) se incluya en la matriz de valores de propiedad del destinatario. 
  
Las propiedades de un destinatario son una combinación de propiedades de libreta de direcciones y propiedades de mensaje. Las propiedades de destinatario pueden aplicarse a todos los mensajes de un destinatario determinado o solo al mensaje actual. Tanto el almacén de mensajes como los proveedores de transporte pueden establecer propiedades de destinatario. 
  
Cada destinatario debe tener un conjunto principal de propiedades en su matriz de valores de propiedad cuando el mensaje esté listo para enviarse. El conjunto necesario de propiedades de destinatario incluyen:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
Estas propiedades se usan para obtener acceso al destinatario, enviarle mensajes y compararlo con otros. No todas estas propiedades deben estar disponibles inmediatamente. Puede agregar un destinatario inicialmente sin conocer su identificador de entrada, basándose en el proceso de resolución de nombres para asignar esta propiedad. En algún momento antes de enviar un mensaje, llama a [IAddrBook::ResolveName](iaddrbook-resolvename.md) para asegurarte de que se resuelvan todos los destinatarios de la lista de destinatarios. Para obtener más información, vea [Resolving a Recipient Name](resolving-a-recipient-name.md).
  
Las listas de destinatarios se pueden crear a partir de usuarios de mensajería o entradas de listas de distribución en un contenedor de libreta de direcciones o desde uno solo. Los one-offs son destinatarios que se crean como entradas temporales que se usan solo para dirigir un único mensaje o como entradas que se van a agregar a una libreta de direcciones personal. MAPI define el formato de un identificador de entrada y una dirección únicos. Para obtener más información acerca de estos [formatos,](one-off-entry-identifiers.md)vea Direcciones de un solo [uso](one-off-addresses.md) e Identificadores de entrada de un solo uso .
  
Puede permitir a los usuarios crear sus listas de destinatarios:
  
- Solo con entradas de la libreta de direcciones.
    
- Solo con entradas únicas.
    
- Con una combinación de destinatarios de libreta de direcciones y one-offs.
    
 **Para crear una lista de destinatarios mediante el cuadro de diálogo dirección común**
  
1. Asigne una [estructura ADRPARM](adrparm.md) y un puntero a una [estructura ADRLIST.](adrlist.md) 
    
2. Cero la memoria en la **estructura ADRPARM** y establezca el **puntero ADRLIST** en NULL. 
    
3. Llama [a IAddrBook::Address](iaddrbook-address.md) para mostrar el cuadro de diálogo dirección y rellenar la **estructura ADRPARM.** 
    
4. Llama [a IMessage::ModifyRecipients](imessage-modifyrecipients.md)y pasa el **puntero ADRLIST.** Esta estructura contendrá las propiedades de cada uno de los destinatarios seleccionados por el usuario. 
    
 **Para crear una lista de destinatarios mediante programación**
  
1. Asigne una **estructura ADRLIST** que contenga una [estructura ADRENTRY](adrentry.md) para cada uno de los destinatarios que se incluirán en la lista. Haga que **cada estructura ADRENTRY** sea lo suficientemente grande como para contener cada una de las propiedades necesarias **y PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).
    
2. Para cada destinatario, establezca la matriz de valores de propiedad para su **miembro aEntries** en la **estructura ADRLIST.** 
    
3. Llama [a IMessage::ModifyRecipients](imessage-modifyrecipients.md) con el MODRECIP_ADD marca establecida. 
    

