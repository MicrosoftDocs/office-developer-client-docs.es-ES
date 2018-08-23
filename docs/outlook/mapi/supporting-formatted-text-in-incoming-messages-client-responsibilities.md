---
title: Compatibilidad con texto con formato en responsabilidades de cliente de los mensajes entrantes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d8fdd9ea4dfbc40d7e800be5e2df666738d2cd23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577460"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Admitir texto con formato en los mensajes entrantes: responsabilidades del cliente

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Como los mensajes se transfieren entre los sistemas de mensajería, la cola MAPI se asegura de que el formato de texto enriquecido permanece sincronizado con el texto del mensaje. La cola MAPI llama a la función de [RTFSync](rtfsync.md) desde dentro de una versión del mensaje que se pasa al proveedor de transporte ajustada. El proveedor de transporte guarda los cambios realizados en el mensaje llamando al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y, a continuación, enruta al destinatario nuevo. 
  
Cuando la aplicación de cliente compatible con RTF del destinatario abre el mensaje para mostrar el texto, debe sincronizar el texto con el formato y abra **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) o **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) , dependiendo de qué propiedad está disponible.
  
 **Para abrir un mensaje, los clientes de tener en cuenta RTF**
  
1. Llame a **RTFSync** para sincronizar el texto del mensaje con el formato si el almacén de mensajes no es compatible con RTF. El indicador RTF_SYNC_BODY_CHANGED debe pasarse en el parámetro _ulFlags_ si la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) falta o se establece en FALSE. Trabajar con almacenes de mensaje RTF compatibles de los clientes no necesitan realizar la llamada **RTFSync** debido a que el almacén de mensajes se ocupa de ella. 
    
2. Llamar a [IMAPIProp::SaveChanges](imapiprop-savechanges.md) si se ha actualizado el texto del mensaje. 
    
3. Llame a [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para abrir la propiedad **PR_RTF_COMPRESSED** . Si **PR_RTF_COMPRESSED** no está disponible, debe abrir en su lugar la propiedad **PR_BODY** para mostrar el contenido del mensaje. 
    
4. Llame a la función [WrapCompressedRTFStream](wrapcompressedrtfstream.md) para crear una versión sin comprimir de los datos RTF comprimidos, si está disponible. 
    
5. Mostrar los datos RTF sin comprimir o los datos de texto sin formato para el usuario.
    
 **RTFSync** devuelve un valor booleano que indica si se ha actualizado el mensaje. Si este valor devuelve el valor TRUE, llame a **SaveChanges** en algún momento para realizar la actualización permanente. La llamada no tiene que estar inmediatamente después de que devuelve **RTFSync** . 
  
> [!NOTE]
> Debido a que tantos componentes controlan el texto con formato antes de recibirla, hay la posibilidad de daños. Este daño podría procedentes del proveedor de almacenamiento de mensajes, una aplicación de terceros, una puerta de enlace o un error de transmisión. 
  

