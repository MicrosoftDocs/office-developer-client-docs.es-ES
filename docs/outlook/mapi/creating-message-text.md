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
  
Aunque algunos mensajes no están hechos de nada más que una lista de destinatarios y una línea de asunto, el contenido de la mayoría de los mensajes, específicamente IPM. Note messages, includes text. El texto del mensaje puede ser sin formato o estar almacenado en tres propiedades: **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Si el cliente está basado en texto sin formato, establezca **PR \_ BODY**. Si admite texto con formato en formato de  texto enriquecido (RTF), establezca PR_RTF_COMPRESSED solo o **bien PR_RTF_COMPRESSED** y **PR \_ BODY**, en función del proveedor de almacenamiento de mensajes que use. Cuando un cliente compatible con RTF usa un almacén de mensajes compatible con RTF, establece PR_RTF_COMPRESSED **solo.** Cuando un cliente compatible con RTF usa un almacén de mensajes no compatible con RTF, establece ambas propiedades. Si el cliente admite HTML, establezca la **PR_HTML** cliente. 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Determinar si el almacén de mensajes admite el formato de texto enriquecido
  
1. Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar la **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
    
2. Compruebe si hay STORE_RTF_OK bits. Si STORE_RTF_OK se establece, el proveedor del almacén de mensajes admite texto RTF. Si no se establece, el proveedor de almacenamiento de mensajes solo admite texto sin formato.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Determinar si el almacén de mensajes admite HTML
  
1. Llame al método [IMAPIProp::GetProps](imapiprop-getprops.md) del almacén de mensajes para recuperar **PR_STORE_SUPPORT_MASK** propiedad. 
    
2. Compruebe si hay STORE_HTML_OK bits. Si STORE_HTML_OK se establece, el proveedor de al almacenamiento de mensajes admite texto HTML. 
    
## <a name="set-pr_rtf_compressed"></a>Establecer pr \_ RTF_COMPRESSED
  
1. Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del mensaje para abrir la propiedad **PR_RTF_COMPRESSED,** especificando IID_IStream como identificador de interfaz y estableciendo la marca MAPI_CREATE mensaje. 
    
2. Llama a [la función WrapCompressedRTFStream](wrapcompressedrtfstream.md) y pasa la marca STORE_UNCOMPRESSED_RTF si el bit STORE_UNCOMPRESSED_RTF está establecido en la propiedad PR_STORE_SUPPORT_MASK del **almacén de** mensajes. 
    
3. Libere la secuencia original llamando a su método ** IUnknown::Release **. 
    
4. Llama a ** IStream::Write ** o **IStream::CopyTo** para escribir el texto del mensaje en la secuencia devuelta desde **WrapCompressedRTFStream**.
    
5. Llama a **los métodos Commit** **y Release** en la secuencia devuelta desde el **método OpenProperty.** 
    
En este punto, si el proveedor de almacenamiento de mensajes admite RTF, ha hecho todo lo necesario. Puede depender del proveedor del almacén de mensajes para controlar la sincronización del contenido y el formato del mensaje y para crear la propiedad **PR \_ BODY** si es necesario. Los almacenes de mensajes rtf-aware llaman [a RTFSync](rtfsync.md) para controlar la sincronización. Si la marca de SYNC_BODY_CHANGED RTF se establece en TRUE, el proveedor volverá a \_ compilar **la PR_BODY** propiedad. 
  
Si el proveedor del almacén de mensajes no admite RTF, también debe agregar contenido de mensajes que no sea RTF estableciendo la **propiedad PR_BODY** mensaje. 
  
## <a name="set-pr_html"></a>Establecer PR_HTML
  
1. Llame al [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la **PR_HTML** con la **interfaz IStream.** 
    
2. Llame **a IStream::Write** para escribir los datos de texto del mensaje en la secuencia devuelta desde **OpenProperty**. 
    
3. Llama **a IStream::Commit** **e IUnknown::Release** en la secuencia para confirmar los cambios y liberar su memoria. 
    
## <a name="set-pr_body"></a>Establecer PR_BODY
  
1. Llame al [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir **la PR_BODY** con la **interfaz IStream.** 
    
2. Llame **a IStream::Write** para escribir los datos de texto del mensaje en la secuencia devuelta desde **OpenProperty**. 
    
3. Llame a [la función RTFSync](rtfsync.md) para sincronizar el texto con el formato. Dado que se trata de un mensaje nuevo, establezca las marcas RTF_SYNC_RTF_CHANGED y RTF_SYNC_BODY_CHANGED para indicar que tanto la versión RTF como la versión de texto sin formato del texto del mensaje han cambiado. **RTFSync** establecerá varias propiedades relacionadas que el proveedor de almacenamiento de mensajes requiere, como **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) y las escribirá en el mensaje.
    
4. Llama **a IStream::Commit** **e IUnknown::Release** en la secuencia para confirmar los cambios y liberar su memoria. 
    

