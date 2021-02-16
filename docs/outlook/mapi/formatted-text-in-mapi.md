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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408092"
---
# <a name="formatted-text-in-mapi"></a>Texto con formato de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El texto de un mensaje se puede almacenar y transmitir mediante texto sin formato o texto con formato. El texto con formato mejora el texto del mensaje modificando su apariencia con, por ejemplo, una o más fuentes, tamaños de fuente o colores de texto. Se recomienda que todos los clientes y, siempre que sea posible, todos los proveedores de almacenamiento de mensajes, admitan texto con formato. La compatibilidad con texto con formato en mensajes agrega valor al mejorar la legibilidad de los mensajes y hacer que el control de mensajes sea más fácil y eficaz.
  
El texto con formato se puede implementar de varias maneras. La forma más común es con el formato de texto enriquecido (RTF). MAPI define tres propiedades transmitibles para contener información de texto del mensaje: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) para texto sin formato, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) para HTML y **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) para texto RTF que se ha comprimido. Dado que la versión con formato de un texto de mensaje puede tener el doble de tamaño que la versión sin formato, el texto RTF se comprime antes de que se transfiera con el mensaje y se almacene en la propiedad **PR_RTF_COMPRESSED.** Cuando es el momento de mostrar el mensaje en la pantalla, se descomprime con una función de utilidad proporcionada por MAPI. 
  
MAPI define estas dos propiedades de texto de mensaje y mecanismos de conversión entre ellos para que los clientes compatibles con RTF puedan interoperar con clientes y sistemas de mensajería que no admiten texto con formato.
  
### 

[Sincronización de texto y formato](synchronizing-text-and-formatting.md)
  
> Describe cómo mantener el texto del mensaje RTF sincronizado con el formato.
    
[Compatibilidad con texto con formato en mensajes salientes: responsabilidades del cliente](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> Describe las responsabilidades de la aplicación cliente para admitir texto con formato en los mensajes salientes.
    
[Admitir texto con formato en mensajes entrantes: responsabilidades del cliente](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> Describe las responsabilidades de la aplicación cliente para admitir texto con formato en los mensajes entrantes.
    
[Compatibilidad con texto con formato: responsabilidades del almacén de mensajes](supporting-formatted-text-message-store-responsibilities.md)
  
> Describe las responsabilidades del almacén de mensajes para admitir texto con formato.
    
[Compatibilidad con texto con formato: representación de datos adjuntos](supporting-formatted-text-rendering-attachments.md)
  
> Describe cómo elegir dónde se representan los datos adjuntos.
    
[Compatibilidad con texto con formato: responsabilidades de puerta de enlace](supporting-formatted-text-gateway-responsibilities.md)
  
> Describe las responsabilidades de la puerta de enlace para los mensajes de texto con formato salientes y entrantes.
    

