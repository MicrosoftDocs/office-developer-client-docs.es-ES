---
title: Admitir texto con formato en los mensajes salientes responsabilidades del cliente
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
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Admitir texto con formato en los mensajes salientes: responsabilidades del cliente

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente establecen la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o la propiedad **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para un mensaje saliente. Los clientes que solo admiten texto sin formato solo establecen la propiedad **PR_BODY** . Los clientes compatibles con el formato de texto enriquecido (RTF) pueden establecer las propiedades **PR_BODY** y **PR_RTF_COMPRESSED** , o solo **PR_RTF_COMPRESSED**, según el proveedor de almacenamiento de mensajes que se use. Los clientes compatibles con HTML establecen la propiedad **PR_HTML** . 
  
Es importante que un cliente Compruebe la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del almacén de mensajes para determinar si el almacén admite RTF. Si el almacén de mensajes no es compatible con RTF, un cliente compatible con RTF establece las propiedades **PR_BODY** y **PR_RTF_COMPRESSED** para cada mensaje saliente. 
  
Si el almacén de mensajes es compatible con RTF, solo se debe establecer la propiedad **PR_RTF_COMPRESSED** . 
  
 **Para establecer PR_RTF_COMPRESSED y asegurarse de que el proceso de sincronización se produce según sea necesario, los clientes que usan el formato RTF**
  
1. Llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_RTF_COMPRESSED** , estableciendo las marcas MAPI_CREATE y MAPI_MODIFY. MAPI_CREATE garantiza que todos los datos nuevos reemplazan los datos antiguos y MAPI_MODIFY permite realizar esos reemplazos. 
    
2. Llame a la función [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , pasando STORE_UNCOMPRESSED_RTF si el almacén de mensajes establece el bit STORE_UNCOMPRESSED_RTF en su propiedad **PR_STORE_SUPPORT_MASK** , para obtener una versión sin comprimir del **PR_RTF_COMPRESSED **secuencia devuelta desde **OpenProperty**.
    
3. Escriba los datos de texto del mensaje en la secuencia descomprimida devuelta desde **WrapCompressedRTFStream**.
    
4. Confirmar y liberar las secuencias comprimidas y sin comprimir.
    
En este punto, si el proveedor de almacenamiento de mensajes admite RTF, habrá hecho todo lo necesario. Puede depender del proveedor de almacenamiento de mensajes para controlar el proceso de sincronización y la creación de la propiedad **PR_BODY** , si es necesario. Sin embargo, si el proveedor de almacenamiento de mensajes no admite RTF, debe llamar a la función [RTFSync](rtfsync.md) para sincronizar el texto con el formato, estableciendo la marca RTF_SYNC_RTF_CHANGED. 
  

