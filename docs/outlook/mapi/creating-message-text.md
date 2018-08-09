---
title: Creación de texto del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 38be3bc2df8931ca45da12e43436377545e8a977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816642"
---
# <a name="creating-message-text"></a>Creación de texto del mensaje

**Hace referencia a**: Outlook 
  
Aunque algunos mensajes se componen de nada más que una lista de destinatarios y una línea de asunto, el contenido de la mayoría de los mensajes, específicamente IPM. Tenga en cuenta los mensajes, incluye texto. Mensaje de texto puede ser sin formato o con formato y se almacena en tres propiedades: **PR\_cuerpo** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si el cliente está basado en texto sin formato, establezca **PR\_cuerpo**. Si admite texto con formato en el formato de texto enriquecido (RTF), establecer **PR_RTF_COMPRESSED** o ambos **PR_RTF_COMPRESSED** y **PR\_cuerpo**, dependiendo de que el proveedor de almacenamiento de mensaje que va a usar. Cuando un cliente compatible con RTF está usando un almacén de mensajes compatible con RTF, Establece sólo **PR_RTF_COMPRESSED** . Cuando un cliente compatible con RTF está usando un almacén de mensajes compatible con RTF, Establece las dos propiedades. Si el cliente es compatible con HTML, establezca la propiedad **PR_HTML** . 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Determinar si el almacén de mensajes es compatible con el formato de texto enriquecido
  
1. Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
    
2. Compruebe si el bit STORE_RTF_OK. Si se establece STORE_RTF_OK, el proveedor de almacenamiento de mensaje admite texto RTF. Si no está establecido, el proveedor de almacén de mensajes es compatible con sólo texto sin formato.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Determinar si el almacén de mensajes es compatible con HTML
  
1. Llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_STORE_SUPPORT_MASK** . 
    
2. Compruebe si el bit STORE_HTML_OK. Si se establece STORE_HTML_OK, el proveedor de almacenamiento de mensaje admite texto HTML. 
    
## <a name="set-prrtfcompressed"></a>Establecer PR\_RTF_COMPRESSED
  
1. Llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del mensaje para abrir la propiedad **PR_RTF_COMPRESSED** , especificando IID_IStream como el identificador de interfaz y estableciendo el indicador MAPI_CREATE. 
    
2. Llame a la función [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , pasando el indicador STORE_UNCOMPRESSED_RTF si está establecido el bit STORE_UNCOMPRESSED_RTF en propiedad **PR_STORE_SUPPORT_MASK** del almacén de mensajes. 
    
3. La versión de la secuencia original mediante una llamada a su ** IUnknown:: Release ** (método). 
    
4. Llamar a ninguno ** IStream::Write ** o **IStream:: CopyTo** para escribir el texto del mensaje en la secuencia devuelta desde **WrapCompressedRTFStream**.
    
5. Llamar a los métodos de **confirmación** y la **versión** en la secuencia devuelta desde el método **OpenProperty** . 
    
En este momento, si el proveedor de almacén de mensajes es compatible con RTF, ha realizado todo lo que es necesario. Puede confiar en el proveedor de almacenamiento de mensajes para controlar la sincronización del contenido del mensaje y el formato y para crear el **PR\_cuerpo** (propiedad) si es necesario. Los almacenes de mensajes RTF para llamar a [RTFSync](rtfsync.md) para controlar la sincronización. Si el formato RTF\_marca SYNC_BODY_CHANGED se establece en TRUE, el proveedor va a volver a calcular la propiedad **PR_BODY** . 
  
Si su proveedor de almacén de mensajes no es compatible con RTF, también debe agregar el contenido del mensaje no RTF estableciendo la propiedad **PR_BODY** . 
  
## <a name="set-prhtml"></a>Establecer PR_HTML
  
1. Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_HTML** con la interfaz **IStream** . 
    
2. Llame a **IStream::Write** para escribir los datos de texto del mensaje en la secuencia devuelta desde **OpenProperty**. 
    
3. Llamar a **IStream:: Commit** e **IUnknown:: Release** en la secuencia para confirmar los cambios y liberar su memoria. 
    
## <a name="set-prbody"></a>Establecer PR_BODY
  
1. Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_BODY** con la interfaz **IStream** . 
    
2. Llame a **IStream::Write** para escribir los datos de texto del mensaje en la secuencia devuelta desde **OpenProperty**. 
    
3. Llame a la función [RTFSync](rtfsync.md) para sincronizar el texto con el formato. Puesto que se trata de un nuevo mensaje, establecer marcadores de la RTF_SYNC_RTF_CHANGED y el RTF_SYNC_BODY_CHANGED para indicar que ha cambiado la versión RTF y texto sin formato del texto del mensaje. **RTFSync** va a establecer las propiedades relacionadas que requiere el proveedor de almacenamiento de mensajes, como **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) y escribirlos en el mensaje.
    
4. Llamar a **IStream:: Commit** e **IUnknown:: Release** en la secuencia para confirmar los cambios y liberar su memoria. 
    

