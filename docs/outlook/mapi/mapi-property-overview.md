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
ms.openlocfilehash: 99887bab2b576e6e6c05414ee9daf1bd6e8d0463
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328204"
---
# <a name="mapi-property-overview"></a>Información general sobre MAPI (propiedad)

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una propiedad es un atributo de un objeto MAPI. Las propiedades describen algo sobre el objeto, como la línea de asunto de un mensaje o el tipo de dirección de un usuario de mensajería. MAPI define muchas propiedades, algunas para describir muchos objetos y otras que solo son adecuadas para un objeto de un tipo determinado. Los clientes y los proveedores de servicios pueden extender el conjunto de propiedades predefinidas de MAPI mediante la creación de nuevas propiedades personalizadas. Los clientes pueden definir propiedades para describir nuevas clases de mensajes, y los proveedores de servicios pueden definir propiedades para exponer las características únicas de su sistema de mensajería.
  
Las propiedades pueden ser persistentes o temporales. Las propiedades que se conservan de una sesión a la sesión se pueden almacenar con los datos de sus objetos o en el perfil. Las propiedades temporales solo existen mientras dure la sesión actual. 
  
Los clientes y los proveedores de servicios pueden mostrar propiedades a los usuarios con una tabla o una hoja de propiedades. Las tablas proporcionan a los usuarios una vista de solo lectura de algunas de las propiedades que pertenecen a varios objetos. Los datos se muestran en formato de fila y columna, donde cada fila representa un objeto y cada columna como una propiedad. Las hojas de propiedades son cuadros de diálogo con fichas que muestran las propiedades relacionadas de un solo objeto. Las hojas de propiedades pueden proporcionar acceso de solo lectura o de lectura y escritura a los datos. El hecho de que un usuario tenga permiso para realizar cambios depende del implementador de la hoja de propiedades.
  
La interfaz [IMAPIProp](imapipropiunknown.md) es la interfaz principal para trabajar con propiedades. Todos los objetos que admiten propiedades implementan **IMAPIProp**. **IMAPIProp** incluye métodos para recuperar valores de propiedades, copiar propiedades, realizar cambios y guardar los cambios, asignar entre nombres de propiedad y sus identificadores, y recuperar información sobre un error anterior. 
  
Hay varias estructuras de datos para describir propiedades e información sobre propiedades. Las estructuras que se usan con más frecuencia son la estructura [SPropValue](spropvalue.md) y la estructura [SPropTagArray](sproptagarray.md) . La estructura **SPropValue** contiene los tres datos que describen una propiedad: 
  
- Datos o valor de la propiedad.
    
- Tipo de datos del valor de la propiedad, como Integer o Boolean. 
    
- Valor numérico dentro de un intervalo determinado que identifica de forma exclusiva la propiedad y el componente responsable de su mantenimiento. Por ejemplo, hay un rango que contiene las propiedades del contenido de los mensajes definidos por MAPI y otro intervalo para contener las propiedades del contenido de los mensajes definidas por un cliente para una clase de mensaje personalizada. 
    
El tipo de propiedad y el identificador se combinan en un único componente denominado etiqueta de propiedad. Las etiquetas de propiedad son constantes que se pueden usar para hacer referencia fácilmente a la propiedad. Las etiquetas de propiedad para las propiedades definidas por MAPI se incluyen en MAPITAGS. H y en el miembro **ulPropTag** de una estructura **SPropValue** . Los clientes y los proveedores de servicios usan etiquetas de propiedad para identificar, recuperar y actualizar las propiedades correspondientes. 
  
La estructura **SPropTagArray** es una matriz contada de etiquetas de propiedad. Muchos de los métodos de **IMAPIProp** y otras interfaces usan una estructura **SPropTagArray** para describir propiedades. 
  
## <a name="see-also"></a>Vea también



[Conceptos de MAPI](mapi-concepts.md)

