---
title: Información general del identificador de propiedad MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 29626f49365a0f37f1e13d965c62bfd5ad0fb774
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414700"
---
# <a name="mapi-property-identifier-overview"></a>Información general del identificador de propiedad MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un identificador de propiedad es un número que se usa para indicar para qué se usa una propiedad y quién es responsable de ella. Los identificadores de propiedad se dividen por MAPI en intervalos; donde un identificador se encuentra en el intervalo indica su uso y propiedad. 
  
El intervalo de identificadores de propiedad se ejecuta 0x0001 a 0xFFFF. Los identificadores de 0x0000 y 0xFFFF se reservan en todos los casos, lo que significa que estos identificadores deben permanecer sin usar. El intervalo de propiedades definido por MAPI se ejecuta de 0x0001 a 0x3FFF. Estas propiedades se denominan propiedades definidas por MAPI. El intervalo 0x4000 a 0x7FFF pertenece a propiedades de mensaje y destinatario, y los clientes o proveedores de servicios pueden definir propiedades en este intervalo. Las propiedades del intervalo de 0x0001 a 0x7FFF se denominan propiedades etiquetadas. Más allá de 0x8000 es el intervalo de lo que se conoce como propiedades con nombre o propiedades que incluyen un identificador único global (GUID) de 32 bits y una cadena de caracteres Unicode o un valor numérico. Los clientes pueden usar propiedades con nombre para personalizar su conjunto de propiedades.
  
Los proveedores de servicios pueden definir propiedades de perfil seguro en el intervalo 0x67F0 a través de 0x67FF. Las propiedades de perfil seguro se usan para la información que requiere protección adicional, como las contraseñas. Estas propiedades se pueden ocultar y cifrar. Si las propiedades seguras se incluyen o no en la lista predeterminada de propiedades devueltas por el método [IMAPIProp::GetPropList](imapiprop-getproplist.md) depende de la implementación del proveedor. Por lo general, estas propiedades no se incluyen. La [interfaz IProfSect : IMAPIProp](iprofsectimapiprop.md) se usa para obtener acceso a las propiedades de una sección de perfil, incluidas las propiedades seguras. 
  
Algunos de los intervalos de propiedades están restringidos a propiedades transmitibles o propiedades no transmitibles. Las propiedades transmitibles se transfieren con un mensaje; Las propiedades no transmitibles no se transfieren con un mensaje. Las propiedades no transmitibles normalmente contienen información que solo es de valor para los clientes y proveedores de servicios que operan con la sesión actual. Estas propiedades no serían necesariamente útiles para otro sistema de mensajería y otro conjunto de proveedores de servicios. El concepto de propiedades transmitibles se aplica principalmente a los proveedores de transporte. Para determinar si una propiedad es transmitible o no, pase su etiqueta de propiedad a la macro **FIsTransmittable,** definida en el archivo de encabezado Mapitags.h. 
  
Para obtener una descripción completa de los intervalos de identificadores, vea [Property Identifier Ranges](property-identifier-ranges.md).
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

