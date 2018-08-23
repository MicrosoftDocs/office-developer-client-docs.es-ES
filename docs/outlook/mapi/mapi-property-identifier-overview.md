---
title: Información general sobre el identificador de propiedad MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8cf2f08a69ee87c40789b764596e514c91483c2e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563159"
---
# <a name="mapi-property-identifier-overview"></a>Información general sobre el identificador de propiedad MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un identificador de la propiedad es un número que se usa para indicar una propiedad que se usa para y quién es responsable de ella. Identificadores de propiedad se dividen por MAPI en intervalos; donde se encuentra un identificador en el intervalo indica su uso y la propiedad. 
  
El intervalo de identificadores de propiedad se ejecuta desde 0 x 0001 a través de 0xFFFF. Identificadores de las propiedades 0 x 0000 y 0xFFFF están reservados en todos los casos, lo que significa que estos identificadores deben permanecer sin usar. El intervalo para propiedades definidas por MAPI se ejecuta desde 0 x 0001 a 0x3FFF. Estas propiedades se conocen como propiedades definidas por MAPI. El intervalo de 0 x 4000 a 0x7FFF pertenece al mensaje y las propiedades de destinatarios y los clientes o proveedores de servicios pueden definir las propiedades de este intervalo. Propiedades del rango de 0 x 0001 a 0x7FFF se conocen como propiedades con etiqueta. Más allá de 0 x 8000 es lo que se conoce como propiedades con nombre o propiedades que incluyen un identificador único global (GUID) de 32 bits y una cadena de caracteres Unicode o el valor numérico del intervalo. Los clientes pueden usar propiedades con nombre para personalizar su conjunto de propiedades.
  
Proveedores de servicios pueden definir las propiedades de perfil seguro en el intervalo de 0x67F0 a través de 0x67FF. Seguro perfil de propiedades se utilizan para obtener información que requiere protección adicional, como las contraseñas. Estas propiedades pueden ser ocultas y cifradas. Si se incluyen las propiedades seguras en la lista predeterminada de las propiedades devueltas por el método [IMAPIProp::GetPropList](imapiprop-getproplist.md) depende de la implementación del proveedor. Normalmente, estas propiedades no se incluyen. El [IProfSect: IMAPIProp](iprofsectimapiprop.md) interfaz se usa para obtener acceso a las propiedades de una sección de perfil, incluidas las propiedades de seguras. 
  
Algunos de los intervalos de la propiedad están restringidos a propiedades transmisible o propiedades nontransmittable. Propiedades transmisible se transfieren con un mensaje; propiedades de nontransmittable no se transfieren con un mensaje. Propiedades de Nontransmittable normalmente contienen información que es de valor sólo para los clientes y proveedores de servicios operativos con la sesión actual. Estas propiedades no sería necesariamente útiles a otro sistema de mensajería y otro conjunto de proveedores de servicios. El concepto de propiedades transmisible se aplica principalmente a los proveedores de transporte. Para determinar si una propiedad es transmisible o no, pase su etiqueta de la propiedad a la macro **FIsTransmittable** , definida en el archivo de encabezado Mapitags.h. 
  
Para obtener una descripción completa de los intervalos de identificador, vea [Intervalos de identificador de propiedad](property-identifier-ranges.md).
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

