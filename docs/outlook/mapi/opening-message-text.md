---
title: Texto del mensaje de apertura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7a2dbe8d2143fd330ae1f5ca5804e30b79909576
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569417"
---
# <a name="opening-message-text"></a>Texto del mensaje de apertura

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El texto de un mensaje se almacena en su **PR\_cuerpo** (propiedad) o **PR\_RTF\_COMPRIMIDO** (propiedad). Para obtener más información, vea **PR\_cuerpo** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), y **PR\_RTF\_COMPRIMIDO** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si admite el formato de texto enriquecido (RTF), abra **PR\_RTF_COMPRESSED**. Si no se admiten RTF, abra **PR\_cuerpo**. Debido a que el texto de un mensaje puede ser grande, independientemente de si o no tiene el formato, use **IMAPIProp::OpenProperty** para abrir estas propiedades. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Para mostrar con formato de texto del mensaje
  
1. Si está utilizando un almacén de mensajes de tener en cuenta que no sean RTF, tal como se indica por la ausencia de la marca STORE_RTF_OK en propiedad de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la tienda:
    
    1. Llamar al método **IMAPIProp::GetProps** del mensaje para recuperar la propiedad **PR_RTF_IN_SYNC** . Para obtener más información, vea [IMAPIProp::GetProps](imapiprop-getprops.md) y **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Llame a RTFSync para sincronizar la propiedad del mensaje PR_BODY con la propiedad **PR_RTF_COMPRESSED** . Para obtener más información, vea [RTFSync](rtfsync.md), **PR_BODY**y **PR_RTF_COMPRESSED**. Pase el RTF_SYNC_BODY_CHANGED marcar si falla la llamada para recuperar **PR_RTF_IN_SYNC** debido a que la propiedad no existe o está establecida en FALSE. 
        
    3. Si **RTFSync** devuelve TRUE, que indica que se han realizado cambios, llamar al método **IMAPIProp::SaveChanges** de los mensajes para almacenarlos permanentemente. Para obtener más información, vea [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
2. Independientemente de si utiliza un mensaje RTF para almacenar:
    
    1. Llame a **IMAPIProp::OpenProperty** para abrir la propiedad **PR_RTF_COMPRESSED** . Para obtener más información, vea [IMAPIProp::OpenProperty](imapiprop-openproperty.md) y **PR_RTF_COMPRESSED**.
        
    2. Si **PR_RTF_COMPRESSED** no está disponible, llamar **OpenProperty** para abrir la propiedad **PR_BODY** . 
        
    3. Llame a la función **WrapCompressedRTFStream** para crear una versión sin comprimir de los datos RTF comprimidos, si está disponible. Para obtener más información, vea [WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Copiar el texto con formato de la secuencia al lugar adecuado en el formulario de mensaje. 
    
### <a name="to-display-plain-message-text"></a>Para mostrar el texto sin formato del mensaje
  
1. Llamar al método **IMAPIProp::GetProps** del mensaje para recuperar la propiedad **PR_BODY** . Para obtener más información, vea [IMAPIProp::GetProps](imapiprop-getprops.md).
    
2. Si **GetProps** devuelve puede ser PT_ERROR para el tipo de propiedad en la estructura de valor de propiedad o MAPI_E_NOT_ENOUGH_MEMORY, llame al método **IMAPIProp::OpenProperty** del mensaje. Pase **PR_BODY** como la etiqueta de propiedad y IID_IStream como el identificador de interfaz. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Copiar el texto sin formato de la secuencia al lugar adecuado en el formulario de mensaje. 
    

