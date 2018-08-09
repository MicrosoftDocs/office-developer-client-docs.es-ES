---
title: Abrir un descriptor de vista
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 525c817cfc3bdcf96455d35025e85486ec8b5b42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818436"
---
# <a name="opening-a-view-descriptor"></a>Abrir un descriptor de vista
  
**Hace referencia a**: Outlook 
  
Muchas carpetas se pueden abrir con una vista normal, una vista predeterminada o cualquier número de vistas personalizadas. Una vista describe cómo mostrar el contenido de una carpeta. Cuando no hay ninguna vista alternativa y cuando se está abriendo la carpeta por primera vez, se usa la vista normal. Cuando existe una vista alternativa, debe usar para abrir la carpeta.
  
Una vista se describe en un mensaje que se conoce como un descriptor de vista. Descriptores de vista se crean normalmente como mensajes asociados y pueden aparecer en las carpetas de la vista personal o común o en cualquier carpeta IPM.
  
### <a name="to-open-a-view-descriptor"></a>Para abrir un descriptor de vista
  
1. Llame a [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para recuperar la tabla de contenido asociada para la carpeta. 
    
2. Crear una restricción que localiza sólo los mensajes con la clase de mensaje que se reserva para los descriptores de vista y llamar a [IMAPITable:: Restrict](imapitable-restrict.md) para limitar la tabla y [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar las filas apropiadas, o...
    
   Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la carpeta para recuperar su propiedad **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)). **PR_DEFAULT_VIEW_ENTRYID** contiene el identificador de entrada para el mensaje que contiene el descriptor de la vista predeterminada de una carpeta. Esta llamada funcionará correctamente si la carpeta admite el uso de la marca MAPI_ASSOCIATED en las llamadas a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) y [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
3. Llame al método [IMsgStore::OpenEntry](imsgstore-openentry.md) con el identificador de entrada del descriptor de vista para abrirlo. 
    

