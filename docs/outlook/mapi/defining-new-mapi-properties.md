---
title: Definición de nuevas propiedades MAPI
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
# <a name="defining-new-mapi-properties"></a>Definición de nuevas propiedades MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
A pesar de la gran cantidad de propiedades proporcionadas por MAPI para su uso por clientes y proveedores de servicios, MAPI permite crear nuevas propiedades si es necesario. Algunos de los escenarios válidos para definir nuevas propiedades públicas incluyen un cliente que crea propiedades para admitir una nueva clase de mensaje y un proveedor de servicios que crea nuevas propiedades para exponer características únicas del sistema de mensajería.
  
Normalmente, no es válido que un proveedor de servicios defina nuevas propiedades para un objeto MAPI existente o una clase de mensaje. Una de las principales ventajas de usar MAPI es que se han configurado identificadores y formatos estándar para un gran número de elementos del sistema de mensajería, lo que permite a los usuarios combinar y combinar perfectamente los proveedores de servicios. Los proveedores de servicios que usan propiedades no estándar no funcionan tan bien con otros proveedores de servicios. 
  
Los clientes pueden crear propiedades de contenido para nuevas clases de mensaje:
  
- Uso de identificadores de propiedad dentro de un intervalo designado para propiedades de contenido específicas de clase de mensaje.
    
    - O -
    
- Uso de propiedades con nombre. 
    
La primera opción es preferible porque no todos los proveedores de servicios admiten propiedades con nombre. MAPI define dos intervalos independientes para que los clientes los usen para las nuevas propiedades de contenido específicas de la clase de mensaje:
  
- 0x6800 para 0x7BFF propiedades transmitibles
    
- 0x7C00 para 0x7FFF propiedades no transmitibles
    
Los identificadores de propiedades deben incluirse en intervalos predefinidos para ayudar a evitar colisiones entre propiedades definidas por distintos proveedores o usuarios. Sin embargo, los usuarios de propiedades de estos intervalos no pueden hacer suposiciones sobre el comportamiento de las propiedades. Todos los clientes que crean una nueva clase de mensaje tienen acceso a estos intervalos; una propiedad con identificador  _xxxx_ puede significar un comportamiento para una clase de mensaje y otro comportamiento para otra clase de mensaje. 
  
Las propiedades con nombre se usan para garantizar que una propiedad específica es única de una clase de mensaje. Los identificadores de propiedad con nombre comienzan en 0x8000 intervalo. Los clientes definen uno o varios nombres y, a continuación, llaman al método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) del almacén de mensajes para asociar un identificador a cada nombre. Los clientes o proveedores de servicios pueden usar propiedades con nombre para definir nuevas propiedades para cualquier objeto solo si el propietario del objeto admite propiedades con nombre. Los usuarios de estas propiedades llaman a **GetIDsFromNames** y a un método **IMAPIProp** relacionado, [GetNamesFromIDs](imapiprop-getnamesfromids.md), para asignar entre un nombre y su identificador.
  
Todas las propiedades, nuevas o existentes, deben usar el conjunto de tipos de propiedades predefinidos. No se pueden agregar nuevos tipos de propiedad y los tipos existentes no se pueden modificar ni eliminar. Las propiedades simples y pequeñas, como las propiedades de un solo carácter o entero de 16 bits, se pueden almacenar en cualquier tipo adecuado. Por ejemplo, los enteros se pueden almacenar como **ULONG** y las cadenas se pueden almacenar como **PT_STRING8**. 
  
Use el **PT_BINARY** para indicar una matriz de bytes contada. Este tipo de propiedad es útil para ampliar los tipos de datos que se pueden almacenar en un objeto. Los bytes se transmiten en secuencia y no se asume el significado de los datos. Cuando una aplicación cliente lee los datos de dicha propiedad, los datos no se modifican de cómo se almacenaron. El cliente debe realizar cualquier intercambio de bytes necesario al mover datos a través de CPU. 
  
## <a name="see-also"></a>Vea también



[Información general sobre MAPI (propiedad)](mapi-property-overview.md)

