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
ms.openlocfilehash: c586d70054542e8d20c90a8caceafabbbb408de8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820485"
---
# <a name="property-names-and-property-sets"></a>Nombres de propiedad y conjuntos de propiedades

  
  
**Hace referencia a**: Outlook 
  
El nombre de cada propiedad con nombre consta de dos partes:
  
- Un identificador único global o GUID, que especifica un conjunto de propiedades.
    
- Una cadena de caracteres Unicode o el valor numérico de 32 bits. 
    
Nombres de propiedades con nombre se describen mediante una estructura [MAPINAMEID](mapinameid.md) . Esta estructura contiene un miembro del grupo de propiedad, un miembro para especificar el nombre de formato numérico o de cadena y un miembro para la identificación de formato que se usa. Dado que el conjunto de propiedades es parte del nombre de la propiedad, no es opcional. MAPI ha definido varios conjuntos de propiedades para que usen los clientes y proveedores de servicios, pero si un conjunto de propiedades existentes es inadecuado, se puede definir un nuevo conjunto de propiedades. Los clientes y proveedores de servicios pueden definir sus propios conjuntos de propiedades mediante una llamada a función [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) . Normalmente, estos conjuntos de propiedades se crean para las aplicaciones cliente personalizadas. 
  
Conjuntos de propiedades de MAPI se representan mediante las siguientes constantes:
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
El conjunto de propiedades PS_MAPI está reservado; se usa por los proveedores de servicio para generar los nombres de propiedades con identificadores por debajo del rango con nombre de propiedad. El conjunto de propiedades PS_PUBLIC_STRINGS se usa en los clientes para propiedades con nombre de los mensajes IPM. Debido a que las propiedades con nombre en el conjunto de propiedades PS_PUBLIC_STRINGS aparecen en la interfaz de usuario de un cliente, los mensajes no visible, como aquellas que pertenecen a la clase de mensaje IPC deben evitar la creación de las propiedades con este conjunto de propiedades con nombre. En su lugar, deben crear propiedades en el intervalo específico de la clase de mensaje, 0x6800 a través de 0x7FFF.
  
Los otros conjuntos de propiedades mantenga propiedades con nombre que describa a los destinatarios que suelen ser miembros de una lista de distribución. Que contiene el mismo tipo de información como las propiedades que están asociadas con las propiedades de la lista de destinatarios, las propiedades de estos conjuntos de propiedades se entienden que las puertas de enlace requieren asignación para un sistema de mensajería de destino. Debido a que hay cinco tipos de información para describir las propiedades, MAPI ha definido cinco conjuntos de propiedades diferentes. Establece un cliente envía un mensaje que debe incluir una dirección y el tipo de dirección para sus miembros de la lista enrutamiento asigna una propiedad con nombre para cada miembro de la PS_ROUTING_EMAIL_ADDRESSES y la propiedad PS_ROUTING_ADDRTYPE. Esto garantiza que la dirección y el tipo de dirección siguen siendo viables cuando se envían a un sistema de mensajería externo.
  
## <a name="see-also"></a>Vea también



[Con el nombre de las propiedades de MAPI](mapi-named-properties.md)

