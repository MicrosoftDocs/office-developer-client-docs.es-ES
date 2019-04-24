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
ms.openlocfilehash: 7f37d65e4beb328c2c92cf0c2ab28586af6bee45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327471"
---
# <a name="formatted-text-in-mapi"></a>Texto con formato de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El texto de un mensaje se puede almacenar y transmitir con texto sin formato o texto con formato. El texto con formato mejora el texto del mensaje al modificar su aspecto con, por ejemplo, una o varias fuentes, tamaños de fuente o colores del texto. Se recomienda que todos los clientes y siempre que sea posible, todos los proveedores de almacenamiento de mensajes admitan texto con formato. La compatibilidad con texto con formato en los mensajes agrega valor mejorando la legibilidad de los mensajes y haciendo que el control de mensajes sea más fácil y eficaz.
  
El texto con formato puede implementarse de varias maneras. La forma más común es con el formato de texto enriquecido (RTF). MAPI define tres propiedades transmitibles para la retención de información de texto del mensaje: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para texto sin formato, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para HTML y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) ) para el texto RTF que se ha comprimido. Debido a que la versión con formato de un texto de mensaje puede ser dos veces mayor que la versión sin formato, el texto RTF se comprime antes de transferirlo con el mensaje y se almacena en la propiedad **PR_RTF_COMPRESSED** . Cuando es el momento de mostrar el mensaje en la pantalla, se descomprime con una función de utilidad proporcionada por MAPI. 
  
MAPI define estas dos propiedades de texto de mensaje y mecanismos de conversión entre ellos para que los clientes compatibles con RTF puedan interoperar con los clientes y los sistemas de mensajería que no admiten el texto con formato.
  
### 

[Sincronizar texto y formato](synchronizing-text-and-formatting.md)
  
> Describe cómo se debe sincronizar el texto del mensaje RTF con el formato.
    
[Admitir texto con formato en los mensajes salientes: responsabilidades del cliente](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Describe las responsabilidades de la aplicación cliente para admitir texto con formato en los mensajes salientes.
    
[Admitir texto con formato en los mensajes entrantes: responsabilidades del cliente](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Describe las responsabilidades de la aplicación cliente para admitir texto con formato en los mensajes entrantes.
    
[Admitir texto con formato: responsabilidades del almacén de mensajes](supporting-formatted-text-message-store-responsibilities.md)
  
> Describe las responsabilidades del almacén de mensajes para admitir texto con formato.
    
[Compatibilidad con texto con formato: representar datos adJuntos](supporting-formatted-text-rendering-attachments.md)
  
> Describe cómo elegir dónde se representan los datos adjuntos.
    
[Compatibilidad con texto con formato: responsabilidades de puerta de enlace](supporting-formatted-text-gateway-responsibilities.md)
  
> Describe las responsabilidades de puerta de enlace para los mensajes entrantes y salientes de texto con formato.
    

