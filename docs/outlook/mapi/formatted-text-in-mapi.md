---
title: Texto con formato de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6b82a755cbf2c8bd0f1d3676d4560e131dce3bd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816872"
---
# <a name="formatted-text-in-mapi"></a>Texto con formato de MAPI

  
  
**Hace referencia a**: Outlook 
  
El texto de un mensaje se puede almacenar y transmite utilizando texto sin formato o texto con formato. Texto con formato mejora el texto del mensaje mediante la modificación de su aspecto con, por ejemplo, uno o más fuentes, tamaños de fuente o los colores de texto. Se recomienda que todos los clientes y siempre que sea posible, todos los proveedores de almacén de mensajes, admiten texto con formato. Compatibilidad con texto con formato en los mensajes agrega valor por mejorar la legibilidad de mensaje y facilitan el control de mensajes y más eficaz.
  
Texto con formato se puede implementar en una variedad de formas. La manera más común es con el formato de texto enriquecido (RTF). MAPI define tres propiedades transmisible para almacenar información de texto de mensaje: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para el texto sin formato, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para HTML y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) para el texto RTF que se ha comprimido. Debido a que la versión de un mensaje de texto con formato dos veces puede ser tan grande como la versión sin formato, se comprime el texto RTF antes de que se transfiere con el mensaje y se almacena en la propiedad **PR_RTF_COMPRESSED** . Cuando sea la hora para mostrar el mensaje en la pantalla, es sin comprimir con una función de utilidad proporcionada por MAPI. 
  
MAPI define estas dos propiedades de texto de mensaje y mecanismos para la conversión entre ellas para que los clientes de tener en cuenta RTF pueden interoperar con los clientes y los sistemas de mensajería que no es compatible con formato de texto.
  
### 

[Sincronizar texto y formato](synchronizing-text-and-formatting.md)
  
> Describe cómo mantener sincronizado con el formato el texto de mensaje RTF.
    
[Admitir texto con formato en los mensajes salientes: responsabilidades del cliente](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Describe las responsabilidades de la aplicación de cliente para la compatibilidad con texto con formato en los mensajes salientes.
    
[Admitir texto con formato en los mensajes entrantes: responsabilidades del cliente](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Describe las responsabilidades de la aplicación de cliente para la compatibilidad con texto con formato en los mensajes entrantes.
    
[Admitir texto con formato: responsabilidades de almacenamiento de mensajes](supporting-formatted-text-message-store-responsibilities.md)
  
> Describe las responsabilidades del almacén de mensaje para admitir texto con formato.
    
[Admitir texto con formato: representar datos adjuntos](supporting-formatted-text-rendering-attachments.md)
  
> Describe cómo elegir donde se representan los datos adjuntos.
    
[Admitir texto con formato: responsabilidades de puerta de enlace](supporting-formatted-text-gateway-responsibilities.md)
  
> Describe las responsabilidades de puerta de enlace para los mensajes de texto con formato entrante y saliente.
    

