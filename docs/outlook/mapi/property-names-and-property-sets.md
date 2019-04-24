---
title: Nombres de propiedad y conjuntos de propiedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328549"
---
# <a name="property-names-and-property-sets"></a>Nombres de propiedad y conjuntos de propiedades

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El nombre de cada propiedad con nombre tiene dos partes:
  
- Identificador único global, o GUID, que especifica un conjunto de propiedades.
    
- Una cadena de caracteres Unicode o un valor numérico de 32 bits. 
    
Los nombres de las propiedades con nombre se describen con una estructura [MAPINAMEID](mapinameid.md) . Esta estructura contiene un miembro de conjunto de propiedades, un miembro para especificar el nombre en formato numérico o de cadena, y un miembro para identificar el formato que se va a usar. Como el conjunto de propiedades forma parte del nombre de la propiedad, no es opcional. MAPI ha definido varios conjuntos de propiedades para que los utilicen los clientes y los proveedores de servicios, pero si un conjunto de propiedades existente es inadecuado, se puede definir un nuevo conjunto de propiedades. Los clientes y los proveedores de servicios pueden definir sus propios conjuntos de propiedades llamando a la función [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) . Por lo general, estos conjuntos de propiedades se crean para aplicaciones cliente personalizadas. 
  
Los conjuntos de propiedades de MAPI se representan mediante las siguientes constantes:
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
El conjunto de propiedades PS_MAPI está reservado; lo usan los proveedores de servicios para generar nombres para propiedades con identificadores por debajo del intervalo de propiedades con nombre. Los clientes usan el conjunto de propiedades PS_PUBLIC_STRINGS para las propiedades con nombre de los mensajes IPM. Dado que las propiedades con nombre en el conjunto de propiedades PS_PUBLIC_STRINGS aparecen en la interfaz de usuario de un cliente, los mensajes no visibles como los que pertenecen a la clase de mensaje IPC deben evitar crear propiedades con nombre con esta propiedad establecida. En su lugar, deben crear propiedades en el rango específico de clase de mensaje, 0x6800 a 0x7FFF.
  
Los otros conjuntos de propiedades contienen propiedades con nombre que describen destinatarios que suelen ser miembros de una lista de enrutamiento. Al contener el mismo tipo de información que las propiedades que se asocian a las propiedades de la lista de destinatarios, las propiedades de estos conjuntos de propiedades se entienden mediante puertas de enlace para requerir asignación para un sistema de mensajería de destino. Debido a que hay cinco tipos de información para describir propiedades, MAPI ha definido cinco conjuntos de propiedades diferentes. Un cliente que envía un mensaje que debe incluir una dirección y un tipo de dirección para los miembros de la lista de enrutamiento asigna una propiedad con nombre para cada miembro de los conjuntos de propiedades PS_ROUTING_EMAIL_ADDRESSES y PS_ROUTING_ADDRTYPE. Esto garantiza que la dirección y el tipo de dirección sigan siendo viables cuando se envíen a un sistema de mensajería externo.
  
## <a name="see-also"></a>Vea también



[Propiedades con nombre MAPI](mapi-named-properties.md)

