---
title: Admitir texto con formato en las responsabilidades del cliente de mensajes salientes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431606"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Admitir texto con formato en mensajes salientes: responsabilidades del cliente

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente establecen la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o la propiedad **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para un mensaje saliente. Los clientes que solo admiten texto sin formato establecen **solo la PR_BODY** propiedad. Los clientes con formato de texto  enriquecido (RTF)  pueden establecer propiedades PR_BODY y PR_RTF_COMPRESSED, o solo **PR_RTF_COMPRESSED**, según el proveedor de almacén de mensajes que se esté utilizando. Los clientes con html establecen la **PR_HTML** propiedad. 
  
Es importante que un cliente compruebe la propiedad PR_STORE_SUPPORT_MASK **del** almacén de mensajes ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para determinar si el almacén admite RTF. Si el almacén de mensajes no es compatible con RTF, un cliente compatible con RTF establece las propiedades **PR_BODY** y **PR_RTF_COMPRESSED** para cada mensaje saliente. 
  
Si el almacén de mensajes es compatible con RTF, solo se debe establecer **la PR_RTF_COMPRESSED** propiedad. 
  
 **Para establecer PR_RTF_COMPRESSED y asegurarse de que el proceso de sincronización se produzca según sea necesario, los clientes con rtf-aware**
  
1. Llame al [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_RTF_COMPRESSED,** estableciendo las marcas MAPI_CREATE y MAPI_MODIFY. MAPI_CREATE garantiza que los nuevos datos reemplazan a los datos antiguos y MAPI_MODIFY permite realizar esos reemplazos. 
    
2. Llame a la función [WrapCompressedRTFStream,](wrapcompressedrtfstream.md) pasando STORE_UNCOMPRESSED_RTF si el almacén de mensajes establece el bit STORE_UNCOMPRESSED_RTF en su propiedad **PR_STORE_SUPPORT_MASK,** para obtener una versión sin comprimir de la secuencia **PR_RTF_COMPRESSED** devuelta de **OpenProperty**.
    
3. Escriba los datos de texto del mensaje en la secuencia sin comprimir devuelta de **WrapCompressedRTFStream**.
    
4. Confirmar y liberar las secuencias sin comprimir y comprimidas.
    
En este momento, si el proveedor del almacén de mensajes admite RTF, ha hecho todo lo necesario. Puede depender del proveedor del almacén de mensajes para controlar el proceso de sincronización y la creación de **la propiedad PR_BODY, si** es necesario. Sin embargo, si el proveedor del almacén de mensajes no admite RTF, debe llamar a la función [RTFSync](rtfsync.md) para sincronizar el texto con el formato, estableciendo la marca RTF_SYNC_RTF_CHANGED mensaje. 
  

