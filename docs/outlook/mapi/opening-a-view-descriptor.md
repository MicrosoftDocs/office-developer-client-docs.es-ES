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
ms.openlocfilehash: ce53e5a91f6fa340728872457eae7f6514e287aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413041"
---
# <a name="opening-a-view-descriptor"></a>Abrir un descriptor de vista
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muchas carpetas se pueden abrir con una vista normal, una vista predeterminada o cualquier número de vistas personalizadas. Una vista describe cómo mostrar el contenido de una carpeta. La vista normal se usa cuando no hay ninguna vista alternativa y cuando se abre la carpeta por primera vez. Cuando existe una vista alternativa, debe usarla para abrir la carpeta.
  
Una vista se describe en un mensaje conocido como descriptor de vista. Los descriptores de vista suelen crearse como mensajes asociados y pueden aparecer en las carpetas de vista común o personal o en cualquier carpeta IPM.
  
### <a name="to-open-a-view-descriptor"></a>Para abrir un descriptor de vista
  
1. Llame [a IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para recuperar la tabla de contenido asociada de la carpeta. 
    
2. Cree una restricción que busque solo los mensajes con la clase de mensaje reservada para descriptores de vista y llame a [IMAPITable::Restrict](imapitable-restrict.md) para limitar la tabla e [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar las filas apropiadas, o...
    
   Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) de la carpeta para recuperar su propiedad **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)). **PR_DEFAULT_VIEW_ENTRYID** contiene el identificador de entrada del mensaje que contiene el descriptor de vista predeterminado de una carpeta. Esta llamada se realizará correctamente si la carpeta admite el uso de la marca MAPI_ASSOCIATED en llamadas a [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) e [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
3. Llame [a IMsgStore::OpenEntry con](imsgstore-openentry.md) el identificador de entrada del descriptor de vista para abrirlo. 
    

