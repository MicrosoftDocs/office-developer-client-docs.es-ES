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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328206"
---
# <a name="mapi-property-identifier-overview"></a>Información general del identificador de propiedad MAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Un identificador de propiedad es un número que se usa para indicar para qué se usa una propiedad y quién es responsable de la misma. Los identificadores de propiedad se dividen en rangos mediante MAPI; donde un identificador cae en el intervalo indica su uso y propiedad. 
  
El intervalo de identificadores de propiedad se ejecuta desde 0x0001 hasta 0xFFFF. Los identificadores de propiedad 0x0000 y 0xFFFF están reservados en todos los casos, lo que significa que estos identificadores deben permanecer sin usar. El rango para las propiedades definidas por MAPI se ejecuta desde 0x0001 hasta 0x3FFF. Estas propiedades se denominan propiedades definidas por MAPI. El rango 0x4000 a 0x7FFF pertenece a las propiedades del destinatario y del mensaje, y los clientes o proveedores de servicios pueden definir propiedades en este intervalo. Las propiedades del intervalo de 0x0001 a 0x7FFF se denominan propiedades etiquetadas. Además de 0x8000, se encuentra el rango para lo que se conoce como propiedades con nombre, o bien propiedades que incluyen un identificador único global (GUID) de 32 y una cadena de caracteres Unicode o un valor numérico. Los clientes pueden usar propiedades con nombre para personalizar su conjunto de propiedades.
  
Los proveedores de servicios pueden definir propiedades de perfil seguro en el intervalo de 0x67F0 a 0x67FF. Las propiedades de perfil seguro se usan para información que requiere protección adicional, como las contraseñas. Estas propiedades se pueden ocultar y cifrar. El hecho de que las propiedades seguras se incluyan en la lista predeterminada de propiedades devueltas por el método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) depende de la implementación del proveedor. Por lo general, estas propiedades no se incluyen. La interfaz [IProfSect: IMAPIProp](iprofsectimapiprop.md) se usa para obtener acceso a las propiedades de una sección de perfil, incluidas las propiedades seguras. 
  
Algunos de los intervalos de propiedades están restringidos a propiedades transmitibles o a propiedades no transmitibles. Las propiedades transmitibles se transfieren con un mensaje; las propiedades no transmitibles no se transfieren con un mensaje. Las propiedades no transmitibles normalmente contienen información que solo es del valor para los clientes y los proveedores de servicios que funcionan con la sesión actual. Estas propiedades no son necesariamente útiles para otro sistema de mensajería y para otro conjunto de proveedores de servicios. El concepto de propiedades transmitibles se aplica principalmente a los proveedores de transporte. Para determinar si una propiedad se transmite o no, pase su etiqueta de propiedad a la macro **FIsTransmittable** , definida en el archivo de encabezado Mapitags. h. 
  
Para obtener una descripción completa de los intervalos de identificadores, consulte [Property Identifier Ranges](property-identifier-ranges.md).
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

