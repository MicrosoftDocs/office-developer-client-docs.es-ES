---
title: Abrir un mensaje de texto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348583"
---
# <a name="opening-message-text"></a>Abrir un mensaje de texto

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El texto de un mensaje se almacena en la propiedad **del\_cuerpo del RP** o en la propiedad **comprimida de\_RTF\_de CP** . Para obtener más información, vea el **cuerpo de PR\_** ([PidTagBody](pidtagbody-canonical-property.md)), el **HTML de PR\_** ([PidTagHtml](pidtaghtml-canonical-property.md)) y el archivo. **\_\_RTF comprimido** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si admite el formato de texto enriquecido (RTF), Abra **PR\_RTF_COMPRESSED**. Si no admite RTF, abra el **cuerpo del\_PR**. Dado que el texto de un mensaje puede ser grande independientemente de si tiene o no formato, use **IMAPIProp:: OpenProperty** para abrir estas propiedades. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Para mostrar el texto del mensaje con formato
  
1. Si usa un almacén de mensajes no compatible con RTF, tal y como indica la ausencia de la marca STORE_RTF_OK en la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la tienda:
    
    1. Llame al método **IMAPIProp:: GetProps** del mensaje para recuperar la propiedad **PR_RTF_IN_SYNC** . Para obtener más información, vea [IMAPIProp:: GetProps](imapiprop-getprops.md) y **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Llame a RTFSync para sincronizar la propiedad PR_BODY del mensaje con la propiedad **PR_RTF_COMPRESSED** . Para obtener más información, vea [RTFSync](rtfsync.md), **PR_BODY**y **PR_RTF_COMPRESSED**. Pasar la marca RTF_SYNC_BODY_CHANGED si se produce un error en la llamada para recuperar **PR_RTF_IN_SYNC** porque la propiedad no existe o se establece en false. 
        
    3. Si **RTFSync** devuelve true (lo que indica que se realizaron cambios), llame al método **IMAPIProp:: SaveChanges** del mensaje para almacenarlos de forma permanente. Para obtener más información, vea [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
    
2. Independientemente de si usa o no un almacén de mensajes que reconozca el formato RTF:
    
    1. Llame a **IMAPIProp:: OpenProperty** para abrir la propiedad **PR_RTF_COMPRESSED** . Para obtener más información, vea [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) y **PR_RTF_COMPRESSED**.
        
    2. Si **PR_RTF_COMPRESSED** no está disponible, llame a **OpenProperty** para abrir la propiedad **PR_BODY** . 
        
    3. Llame a la función **WrapCompressedRTFStream** para crear una versión sin comprimir de los datos RTF comprimidos, si están disponibles. Para obtener más información, vea [WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Copie el texto con formato del flujo en el punto adecuado en el formulario de mensaje. 
    
### <a name="to-display-plain-message-text"></a>Para mostrar texto de mensaje sin formato
  
1. Llame al método **IMAPIProp:: GetProps** del mensaje para recuperar la propiedad **PR_BODY** . Para obtener más información, vea [IMAPIProp:: GetProps](imapiprop-getprops.md).
    
2. Si **GetProps** devuelve PT_ERROR para el tipo de propiedad en la MAPI_E_NOT_ENOUGH_MEMORY o la estructura del valor de la propiedad, llame al método **IMAPIProp:: OpenProperty** del mensaje. Pase **PR_BODY** como la etiqueta Property y IID_IStream como identificador de interfaz. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Copie el texto sin formato del flujo en el punto adecuado del formulario de mensaje. 
    

