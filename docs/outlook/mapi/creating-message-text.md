---
title: Crear el texto del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5b4a4107d6326a61f50a4023ebc2538f699224b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428007"
---
# <a name="creating-message-text"></a>Crear el texto del mensaje

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Aunque algunos mensajes no están formados por nada más que una lista de destinatarios y una línea de asunto, el contenido de la mayoría de los mensajes, en concreto, IPM. Los mensajes de nota incluyen texto. El texto del mensaje puede ser normal o formateado y se almacena en tres propiedades: **PR\_Body** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si el cliente está basado en texto sin formato, establezca el **cuerpo de PR\_**. Si admite texto con formato en el formato de texto enriquecido (RTF), establezca solo **PR_RTF_COMPRESSED** o tanto **PR_RTF_COMPRESSED** como **RP\_Body**, según el proveedor de almacenamiento de mensajes que use. Cuando un cliente compatible con RTF usa un almacén de mensajes con reconocimiento de RTF, sólo establece **PR_RTF_COMPRESSED** . Cuando un cliente compatible con RTF usa un almacén de mensajes que no es compatible con RTF, establece ambas propiedades. Si el cliente admite HTML, establezca la propiedad **PR_HTML** . 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Determinar si el almacén de mensajes admite el formato de texto enriquecido
  
1. Llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
    
2. Compruebe el bit STORE_RTF_OK. Si se establece STORE_RTF_OK, el proveedor de almacenamiento de mensajes admite texto RTF. Si no se establece, el proveedor de almacenamiento de mensajes solo admite texto sin formato.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Determinar si el almacén de mensajes admite HTML
  
1. Llame al método [IMAPIProp:: GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la propiedad **PR_STORE_SUPPORT_MASK** . 
    
2. Compruebe el bit STORE_HTML_OK. Si se establece STORE_HTML_OK, el proveedor de almacenamiento de mensajes admite texto HTML. 
    
## <a name="set-prrtfcompressed"></a>Establecer PR\_RTF_COMPRESSED
  
1. Llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del mensaje para abrir la propiedad **PR_RTF_COMPRESSED** , especificando IID_IStream como identificador de interfaz y configurando la marca MAPI_CREATE. 
    
2. Llame a la función [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , pasando la marca STORE_UNCOMPRESSED_RTF si el bit STORE_UNCOMPRESSED_RTF se establece en la propiedad **PR_STORE_SUPPORT_MASK** del almacén de mensajes. 
    
3. Libere el flujo original llamando a su método * * IUnknown:: Release * *. 
    
4. Llamar a * * IStream:: write * * o **IStream:: CopyTo** para escribir el texto del mensaje en la secuencia devuelta desde **WrapCompressedRTFStream**.
    
5. Llamar a los métodos **commit** y **Release** en la secuencia devuelta desde el método **OpenProperty** . 
    
En este punto, si el proveedor de almacenamiento de mensajes admite RTF, habrá hecho todo lo necesario. Puede depender del proveedor de almacenamiento de mensajes para controlar la sincronización del contenido y el formato del mensaje, y crear la propiedad **del cuerpo del PR\_** si es necesario. Los almacenes de mensajes compatibles con RTF llaman a [RTFSync](rtfsync.md) para controlar la sincronización. Si la marca\_de SYNC_BODY_CHANGED RTF se establece en true, el proveedor volverá a calcular la propiedad **PR_BODY** . 
  
Si su proveedor de almacenamiento de mensajes no admite RTF, también debe agregar contenido de mensaje que no sea RTF estableciendo la propiedad **PR_BODY** . 
  
## <a name="set-prhtml"></a>Establecer PR_HTML
  
1. Llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_HTML** con la interfaz **IStream** . 
    
2. Llamar a **IStream:: Write** para escribir los datos de texto del mensaje en la secuencia devuelta desde **OpenProperty**. 
    
3. Llame a **IStream:: commit** e **IUnknown:: Release** en la secuencia para confirmar los cambios y liberar su memoria. 
    
## <a name="set-prbody"></a>Establecer PR_BODY
  
1. Llame al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_BODY** con la interfaz **IStream** . 
    
2. Llamar a **IStream:: Write** para escribir los datos de texto del mensaje en la secuencia devuelta desde **OpenProperty**. 
    
3. Llame a la función [RTFSync](rtfsync.md) para sincronizar el texto con el formato. Dado que se trata de un nuevo mensaje, establezca los indicadores RTF_SYNC_RTF_CHANGED y RTF_SYNC_BODY_CHANGED para indicar que tanto la versión de texto sin formato como la del texto del mensaje han cambiado. **RTFSync** establecerá varias propiedades relacionadas que requiera el proveedor de almacén de mensajes, como **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), y las escribirá en el mensaje.
    
4. Llame a **IStream:: commit** e **IUnknown:: Release** en la secuencia para confirmar los cambios y liberar su memoria. 
    

