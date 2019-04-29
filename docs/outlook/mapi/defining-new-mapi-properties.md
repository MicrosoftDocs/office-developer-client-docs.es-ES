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
ms.openlocfilehash: 666ee413319765e39e25d586208f764afc93ae6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425018"
---
# <a name="defining-new-mapi-properties"></a>Definir nuevas propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
A pesar de la riqueza de propiedades suministradas por MAPI para que las usen los clientes y los proveedores de servicios, MAPI permite que se creen nuevas propiedades si es necesario. Algunos de los escenarios válidos para definir nuevas propiedades públicas incluyen el cliente que crea propiedades para admitir una nueva clase de mensaje y un proveedor de servicios que crea nuevas propiedades para exponer características únicas del sistema de mensajería.
  
Por lo general, no es válido para un proveedor de servicios definir nuevas propiedades para un objeto o una clase de mensaje existente de MAPI. Una de las principales ventajas de usar MAPI es que se configuran los identificadores y los formatos estándar para un gran número de elementos del sistema de mensajería, lo que permite a los usuarios combinar y asignar los proveedores de servicios de forma transparente. Los proveedores de servicios que usan propiedades no estándar no funcionan tan bien con otros proveedores de servicios. 
  
Los clientes pueden crear propiedades de contenido para nuevas clases de mensaje mediante:
  
- Uso de identificadores de propiedad dentro de un intervalo designado para propiedades de contenido específicas de la clase de mensaje.
    
    - O
    
- Uso de propiedades con nombre. 
    
La primera opción es preferible porque no todos los proveedores de servicios admiten propiedades con nombre. MAPI define dos intervalos distintos para que los clientes los usen para nuevas propiedades de contenido específicas de la clase de mensaje:
  
- 0x6800 a 0x7BFF para propiedades transmitibles
    
- 0x7C00 a 0x7FFF para propiedades no transmitibles
    
Los identificadores de propiedad deben estar en intervalos predefinidos para ayudar a evitar colisiones entre las propiedades definidas por diferentes proveedores o usuarios. Sin embargo, los usuarios de propiedades de estos intervalos no pueden hacer suposiciones como el comportamiento de las propiedades. Cada cliente que crea una nueva clase de mensaje tiene acceso a estos rangos; una propiedad con el identificador _xxxx_ puede significar un comportamiento para una clase de mensaje y otro comportamiento para otra clase de mensaje. 
  
Las propiedades con nombre se usan para garantizar que una propiedad específica es única para una clase de mensaje. Los identificadores de propiedad con nombre comienzan en el intervalo 0x8000. Los clientes definen uno o más nombres y, a continuación, llaman al método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) del almacén de mensajes para asociar un identificador a cada nombre. Los clientes o proveedores de servicios pueden usar las propiedades con nombre para definir nuevas propiedades de cualquier objeto solo si el propietario del objeto admite propiedades con nombre. Los usuarios de estas propiedades llaman a **GetIDsFromNames** y a un método **IMAPIProp** relacionado, [GetNamesFromIDs](imapiprop-getnamesfromids.md), para asignar un nombre y su identificador.
  
Todas las propiedades, nuevas o existentes, deben usar el conjunto de tipos de propiedad predefinidos. No se pueden agregar nuevos tipos de propiedad y los tipos existentes no se pueden modificar ni eliminar. Sencillas, las propiedades pequeñas, como las propiedades de un solo carácter o de enteros de 16 bits, se pueden almacenar en cualquier tipo apropiado. Por ejemplo, los enteros se pueden almacenar como **ULong** y las cadenas se pueden almacenar como **PT_STRING8**. 
  
Use el tipo **PT_BINARY** para indicar una matriz de bytes contada. Este tipo de propiedad es útil para extender los tipos de datos que se pueden almacenar en un objeto. Los bytes se transmiten secuencialmente y no se realizan suposiciones sobre el significado de los datos. Cuando una aplicación cliente lee datos de dicha propiedad, los datos no cambian desde el momento en que se almacenaron. El cliente debe realizar cualquier intercambio de bytes necesario al mover datos entre las CPU. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

