---
title: Definir nuevas propiedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f922ee95cda84311d840aa9de339883c57efba56
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590326"
---
# <a name="defining-new-mapi-properties"></a>Definir nuevas propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
A pesar de la gran cantidad de propiedades suministrada por MAPI para que usen los clientes y proveedores de servicios, MAPI permite nuevas propiedades que se creará si es necesario. Algunos de los escenarios válidos para definir nuevas propiedades públicas incluyen un cliente de creación de propiedades para admitir una nueva clase de mensaje y un proveedor de servicios creación de nuevas propiedades para exponer características exclusivas de mensajería del sistema.
  
Normalmente, no es válido para un proveedor de servicios definir nuevas propiedades para una clase de objeto o un mensaje existente de MAPI. Una de las principales ventajas del uso de MAPI es que los identificadores estándar y formatos para un gran número de sistema de mensajería se establecen elementos de copia de seguridad, permitir a los usuarios sin ningún problema mezclar y hacer coincidir los proveedores de servicios. Proveedores de servicios que se utilizan las propiedades no estándar no funcionan así como con otros proveedores de servicios. 
  
Los clientes pueden crear propiedades de contenido para nuevas clases de mensaje por:
  
- Mediante identificadores de propiedad dentro de un intervalo designado para propiedades de contenido específico de la clase de mensaje.
    
    - O bien -
    
- Uso de propiedades con nombre. 
    
La primera opción es preferible debido a que no todos los proveedores de servicios admiten las propiedades con nombre. MAPI define dos rangos independientes para los clientes que se usará para nuevas propiedades de contenido específico de la clase de mensaje:
  
- 0x6800 a 0x7BFF para propiedades transmisible
    
- 0x7C00 a 0x7FFF para las propiedades de nontransmittable
    
Identificadores de propiedad deben estar comprendido en rangos predefinidos para ayudar a evitar conflictos entre las propiedades definidas por distintos proveedores o los usuarios. Sin embargo, los usuarios de las propiedades de estos intervalos no pueden realizar suposiciones sobre el comportamiento de las propiedades. Cada cliente que crea una nueva clase de mensaje tiene acceso a estos intervalos; una propiedad con identificador _xxxx_ puede significar un comportamiento de una clase de mensaje y el otro comportamiento de otra clase de mensaje. 
  
Propiedades con nombre se utilizan para garantizar que una propiedad concreta es única para una clase de mensaje. Inician de identificadores de propiedad con nombre en el rango de 0 x 8000. Los clientes definición uno o varios nombres y, a continuación, llamar al método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) del almacén de mensajes para asociar un identificador a cada nombre. Propiedades con nombre se pueden usar por los clientes o proveedores de servicios para definir nuevas propiedades para cualquier objeto sólo si el propietario del objeto admite propiedades con nombre. Los usuarios de estas propiedades llamadas **a GetIDsFromNames** y un método **IMAPIProp** relacionado, [GetNamesFromIDs](imapiprop-getnamesfromids.md), para asignar entre un nombre y su identificador.
  
Todas las propiedades, nuevas o existentes, deben usar el conjunto de tipos de propiedad predefinida. No se puede agregar nuevos tipos de propiedad y no pueden ser modificados o eliminados los tipos existentes. Propiedades simples, pequeñas, como las propiedades de entero de 16 bits o de un solo carácter, se pueden almacenar en cualquier tipo apropiado. Por ejemplo, se pueden almacenar números enteros como **ULONG** y cadenas pueden almacenarse como **PT_STRING8**. 
  
Use el tipo **PT_BINARY** para indicar una matriz de bytes contada. Este tipo de propiedad es útil para extender los tipos de datos que se pueden almacenar en un objeto. Bytes se transmiten en secuencia y no se hacen suposiciones sobre el significado de los datos. Cuando una aplicación cliente lee datos fuera de este tipo de propiedad, los datos se ha modificado desde cómo se almacenó. El cliente debe llevar a cabo cualquier byte es necesario intercambiar al mover datos a través de CPU. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

