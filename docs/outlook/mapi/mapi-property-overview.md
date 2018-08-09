---
title: Información general sobre MAPI (propiedad)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e5b23f-1bdb-4fbf-a27d-e3301a359573
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ed11677d09ae5acacced77373b2bca783d1ec0b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818186"
---
# <a name="mapi-property-overview"></a>Información general sobre MAPI (propiedad)

  
  
**Hace referencia a**: Outlook 
  
Una propiedad es un atributo de un objeto MAPI. Las propiedades describen algo sobre el objeto, por ejemplo, la línea de asunto de un mensaje o el tipo de dirección de un usuario de mensajería. MAPI define muchas propiedades, algunas para describir muchos objetos y algunos que sólo son apropiadas para un objeto de un tipo determinado. Los clientes y proveedores de servicios pueden ampliar el conjunto de MAPI de propiedades predefinidas mediante la creación de nuevo, las propiedades personalizadas. Los clientes pueden definir propiedades para describir las nuevas clases de mensaje y los proveedores de servicios pueden definir propiedades para exponer las características exclusivas de su sistema de mensajería.
  
Las propiedades pueden ser persistentes o temporales. Las propiedades que se conservan de una sesión a otra pueden almacenarse con datos de sus objetos o en el perfil. Propiedades temporales sólo existen para la duración de la sesión actual. 
  
Los clientes y proveedores de servicios pueden mostrar las propiedades a los usuarios con una tabla o una hoja de propiedades. Tablas de proporcionan a los usuarios con una vista de solo lectura de algunas de las propiedades que pertenecen a varios objetos. Los datos se muestran en formato de fila y columna, con cada fila que representa un objeto y cada columna de una propiedad. Hojas de propiedades son cuadros de diálogo con fichas que mostrar las propiedades relacionadas para un único objeto. Hojas de propiedades pueden proporcionar como de solo lectura o acceso de lectura y escritura a los datos. Si un usuario tiene permitido realizar cambios es responsabilidad del implementador de la hoja de propiedades.
  
La interfaz de [IMAPIProp](imapipropiunknown.md) es la interfaz principal para trabajar con propiedades. Todos los objetos que admiten propiedades implementar **IMAPIProp**. **IMAPIProp** incluye métodos para recuperar los valores de propiedad, copiando propiedades, realizar cambios y guardar dichos cambios, asignación entre los nombres de propiedad y sus identificadores y recuperar información sobre un error anterior. 
  
Hay varias estructuras de datos para describir las propiedades y obtener información acerca de las propiedades. Las estructuras usadas con más frecuencia son la estructura de [SPropValue](spropvalue.md) y la estructura del [elemento SPropTagArray](sproptagarray.md) . La estructura **SPropValue** contiene las tres partes de la información que describen una propiedad: 
  
- Datos, o el valor de la propiedad.
    
- Tipo de datos del valor de la propiedad, como integer o Boolean. 
    
- Valor numérico dentro de un intervalo determinado que identifican la propiedad y el componente responsable de mantener. Por ejemplo, hay un intervalo para incluir contenido de propiedades definidas por MAPI y otro intervalo para contener propiedades de contenido de mensaje definen por un cliente para una clase de mensaje personalizada del mensaje. 
    
El tipo de propiedad y el identificador se combinan en un solo componente denominado la etiqueta de propiedad. Las etiquetas de propiedad son constantes que se pueden usar para hacer referencia fácilmente a la propiedad. Etiquetas de propiedad para propiedades definidas por MAPI se incluyen en la MAPITAGS. Archivo de encabezado de H y en el miembro **ulPropTag** de una estructura **SPropValue** . Los clientes y proveedores de servicios de usan etiquetas de propiedad para identificar, recuperar y actualizar las propiedades correspondientes. 
  
La estructura del **elemento SPropTagArray** es una matriz unidimensional de etiquetas de propiedad. Muchos de los métodos en **IMAPIProp** y otras interfaces utilizan una estructura de **elemento SPropTagArray** para describir las propiedades. 
  
## <a name="see-also"></a>Vea también



[Conceptos MAPI](mapi-concepts.md)

