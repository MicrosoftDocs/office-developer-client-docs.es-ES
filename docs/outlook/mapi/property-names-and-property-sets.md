---
title: Nombres de propiedades y conjuntos de propiedades
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
# <a name="property-names-and-property-sets"></a>Nombres de propiedades y conjuntos de propiedades

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El nombre de cada propiedad con nombre tiene dos partes:
  
- Un identificador único global, o GUID, que especifica un conjunto de propiedades.
    
- Una cadena de caracteres Unicode o un valor numérico de 32 bits. 
    
Los nombres de las propiedades con nombre se describen mediante [una estructura MAPINAMEID.](mapinameid.md) Esta estructura contiene un miembro del conjunto de propiedades, un miembro para especificar el nombre en formato numérico o de cadena y un miembro para identificar qué formato se usa. Dado que el conjunto de propiedades forma parte del nombre de la propiedad, no es opcional. MAPI ha definido varios conjuntos de propiedades para su uso por parte de clientes y proveedores de servicios, pero si un conjunto de propiedades existente es inadecuado, se puede definir un nuevo conjunto de propiedades. Los clientes y proveedores de servicios pueden definir sus propios conjuntos de propiedades llamando a [la función CoCreateGUID.](https://msdn.microsoft.com/library/ms688568.aspx) Normalmente, estos conjuntos de propiedades se crean para aplicaciones cliente personalizadas. 
  
Los conjuntos de propiedades de MAPI se representan mediante las siguientes constantes:
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
El PS_MAPI de propiedades está reservado; los proveedores de servicios lo usan para generar nombres para propiedades con identificadores por debajo del intervalo de propiedades con nombre. El PS_PUBLIC_STRINGS de propiedades es usado por los clientes para las propiedades con nombre de los mensajes IPM. Dado que las propiedades con nombre del conjunto de propiedades PS_PUBLIC_STRINGS aparecen en la interfaz de usuario de un cliente, los mensajes novisibles como los que pertenecen a la clase de mensaje IPC deben evitar crear propiedades con nombre con este conjunto de propiedades. En su lugar, deben crear propiedades en el intervalo específico de la clase del mensaje, 0x6800 a través de 0x7FFF.
  
Los demás conjuntos de propiedades contienen propiedades con nombre que describen los destinatarios que normalmente son miembros de una lista de enrutamiento. Con el mismo tipo de información que las propiedades asociadas con propiedades de lista de destinatarios, las puertas de enlace entienden que las propiedades de estos conjuntos de propiedades requieren la asignación de un sistema de mensajería de destino. Dado que hay cinco tipos de información para describir propiedades, MAPI ha definido cinco conjuntos de propiedades diferentes. Un cliente que envía un mensaje que debe incluir una dirección y un tipo de dirección para sus miembros de lista de enrutamiento asigna una propiedad con nombre para cada miembro de los conjuntos de propiedades PS_ROUTING_EMAIL_ADDRESSES y PS_ROUTING_ADDRTYPE de enrutamiento. Esto garantiza que la dirección y el tipo de dirección permanecen viables cuando se envían a un sistema de mensajería externo.
  
## <a name="see-also"></a>Vea también



[Propiedades con nombre MAPI](mapi-named-properties.md)

