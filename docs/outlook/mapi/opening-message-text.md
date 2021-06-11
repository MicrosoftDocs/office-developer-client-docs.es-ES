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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407539"
---
# <a name="opening-message-text"></a>Abrir un mensaje de texto

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El texto de un mensaje se almacena en su **propiedad PR \_ BODY** o **pr RTF \_ \_ COMPRESSED.** Para obtener más información, **vea PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) y **PR RTF \_ \_ COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si admite el formato de texto enriquecido (RTF), abra **pr \_ RTF_COMPRESSED**. Si no admite RTF, abra **PR \_ BODY**. Dado que el texto de un mensaje puede ser grande independientemente de si tiene o no formato, use **IMAPIProp::OpenProperty** para abrir estas propiedades. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Para mostrar texto de mensaje con formato
  
1. Si usa un almacén de mensajes no compatible con RTF, como se indica por la ausencia de la marca STORE_RTF_OK en la propiedad PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del almacén:
    
    1. Llame al método **IMAPIProp::GetProps** del mensaje para recuperar la **PR_RTF_IN_SYNC** propiedad. Para obtener más información, vea [IMAPIProp::GetProps](imapiprop-getprops.md) **y PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Llame a RTFSync para sincronizar la propiedad PR_BODY del mensaje con la **PR_RTF_COMPRESSED** propiedad. Para obtener más información, vea [RTFSync](rtfsync.md), **PR_BODY** y **PR_RTF_COMPRESSED**. Pase la RTF_SYNC_BODY_CHANGED si la llamada  para recuperar PR_RTF_IN_SYNC error porque la propiedad no existe o está establecida en FALSE. 
        
    3. Si **RTFSync** devuelve TRUE , que indica que se realizaron cambios, llama al método **IMAPIProp::SaveChanges** del mensaje para almacenarlos de forma permanente. Para obtener más información, [vea IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
2. Independientemente de si está usando un almacén de mensajes compatible con RTF:
    
    1. Llame **a IMAPIProp::OpenProperty** para abrir la **PR_RTF_COMPRESSED** propiedad. Para obtener más información, [vea IMAPIProp::OpenProperty](imapiprop-openproperty.md) y **PR_RTF_COMPRESSED**.
        
    2. Si **PR_RTF_COMPRESSED** está disponible, llama **a OpenProperty** para abrir la **PR_BODY** propiedad. 
        
    3. Llame a **la función WrapCompressedRTFStream** para crear una versión sin comprimir de los datos RTF comprimidos, si está disponible. Para obtener más información, [vea WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Copie el texto con formato de la secuencia en el lugar adecuado en el formulario de mensaje. 
    
### <a name="to-display-plain-message-text"></a>Para mostrar texto de mensaje sin formato
  
1. Llame al método **IMAPIProp::GetProps** del mensaje para recuperar la **PR_BODY** propiedad. Para obtener más información, [vea IMAPIProp::GetProps](imapiprop-getprops.md).
    
2. Si **GetProps** devuelve PT_ERROR para el tipo de propiedad en la estructura de valores de propiedad o MAPI_E_NOT_ENOUGH_MEMORY, llame al método **IMAPIProp::OpenProperty del** mensaje. Pase **PR_BODY** como etiqueta de propiedad y IID_IStream como identificador de interfaz. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Copie el texto sin formato de la secuencia en el lugar adecuado en el formulario de mensaje. 
    

