---
title: Admitir texto con formato en los mensajes entrantes responsabilidades del cliente
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434504"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Admitir texto con formato en los mensajes entrantes: responsabilidades del cliente

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
A medida que los mensajes se transfieren entre sistemas de mensajería, la cola MAPI se asegura de que el formato de texto enriquecido permanezca sincronizado con el texto del mensaje. La cola MAPI llama a la función [RTFSync](rtfsync.md) desde una versión ajustada del mensaje que pasa al proveedor de transporte. El proveedor de transporte guarda los cambios realizados en el mensaje mediante una llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) y, a continuación, lo enruta al nuevo destinatario. 
  
Cuando la aplicación cliente de RTF del destinatario abre el mensaje para mostrar el texto, debe sincronizar el texto con el formato y abrir **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). , en función de la propiedad que esté disponible.
  
 **Para abrir un mensaje, los clientes que reconocen RTF**
  
1. Llamar a **RTFSync** para sincronizar el texto del mensaje con el formato si el almacén de mensajes no es compatible con RTF. La marca RTF_SYNC_BODY_CHANGED debe pasarse en el parámetro _ulFlags_ si falta la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) o si se establece en false. Los clientes que trabajan con almacenes de mensajes conscientes de RTF no tienen que realizar la llamada de **RTFSync** porque el almacén de mensajes se encarga de ello. 
    
2. Llame a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) si se ha actualizado el texto del mensaje. 
    
3. Llame a [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_RTF_COMPRESSED** . Si **PR_RTF_COMPRESSED** no está disponible, debe abrir la propiedad **PR_BODY** en su lugar para mostrar el contenido del mensaje. 
    
4. Llame a la función [WrapCompressedRTFStream](wrapcompressedrtfstream.md) para crear una versión sin comprimir de los datos RTF comprimidos, si están disponibles. 
    
5. Mostrar los datos RTF sin comprimir o los datos de texto sin formato al usuario.
    
 **RTFSync** devuelve un valor booleano que indica si el mensaje se ha actualizado o no. Si este valor devuelve TRUE, llame a **SaveChanges** en algún momento para que la actualización sea permanente. La llamada no tiene que realizarse inmediatamente después de **RTFSync** devuelve. 
  
> [!NOTE]
> Debido a que muchos componentes manejan el texto con formato antes de recibirlo, existe la posibilidad de que se dañen. Este daño puede provenir del proveedor de almacenamiento de mensajes, una aplicación de terceros, una puerta de enlace o un error de transmisión. 
  

