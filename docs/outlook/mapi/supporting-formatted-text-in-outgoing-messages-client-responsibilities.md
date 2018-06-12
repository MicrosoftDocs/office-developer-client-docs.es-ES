---
title: Compatibilidad con texto con formato en responsabilidades de cliente de los mensajes salientes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: d5ce2e6b0f10ff6c2f6fd91ca9f73953f3ee7cd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820781"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Compatibilidad con texto con formato en los mensajes salientes: responsabilidades del cliente

  
  
**Se aplica a**: Outlook 
  
Las aplicaciones cliente de establecer la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o la propiedad **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para un mensaje saliente. Los clientes que admiten sólo texto sin formato establecer sólo la propiedad **PR_BODY** . Formato de texto de Rich (RTF)-tener en cuenta los clientes pueden establecer **PR_BODY** y propiedades **PR_RTF_COMPRESSED** o sólo **PR_RTF_COMPRESSED**, según el mensaje almacenar proveedor que se utiliza. Los clientes compatibles con HTML establecer la propiedad **PR_HTML** . 
  
Es importante para un cliente comprobar la propiedad de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de su almacén de mensajes para determinar si el almacén admite RTF. Si el almacén de mensajes no es compatible con RTF, un cliente compatible con RTF establece las propiedades de la **PR_BODY** y el **PR_RTF_COMPRESSED** para todos los mensajes salientes. 
  
Si el almacén de mensajes es compatible con RTF, sólo **PR_RTF_COMPRESSED** necesita la propiedad va a establecer. 
  
 **Para establecer PR_RTF_COMPRESSED y asegúrese de que la sincronización se produce el proceso como sea necesarios, tener en cuenta RTF clientes**
  
1. Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_RTF_COMPRESSED** , establecer marcadores de la MAPI_CREATE y la MAPI_MODIFY. MAPI_CREATE garantiza que los datos nuevos reemplazan los datos anteriores y MAPI_MODIFY le permite realizar los reemplazos. 
    
2. Llame a la función [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , pasando STORE_UNCOMPRESSED_RTF si el almacén de mensajes establece el bit STORE_UNCOMPRESSED_RTF en su propiedad **PR_STORE_SUPPORT_MASK** , para obtener una versión de la **PR_RTF_COMPRESSED sin comprimir **secuencia devuelto desde **OpenProperty**.
    
3. Escribir los datos de texto del mensaje en la secuencia sin comprimir devuelta desde **WrapCompressedRTFStream**.
    
4. Confirmar y liberar las secuencias sin comprimir y comprimidas.
    
En este momento, si el proveedor de almacén de mensajes es compatible con RTF, ha realizado todo lo que es necesario. Puede confiar en el proveedor de almacenamiento de mensajes para controlar el proceso de sincronización y la creación de la propiedad **PR_BODY** , si es necesario. Sin embargo, si el proveedor de almacén de mensajes no es compatible con RTF, debe llamar a la función [RTFSync](rtfsync.md) para sincronizar el texto con el formato, se establecer el indicador RTF_SYNC_RTF_CHANGED. 
  

