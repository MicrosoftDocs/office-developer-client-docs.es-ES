---
title: Tablas MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7974cae1-10f1-42e9-8be4-c02f2bd86714
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6393de45dbfd130e15a0678f2b6a7f18968dfa03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573218"
---
# <a name="mapi-tables"></a>Tablas MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla MAPI es un objeto MAPI que se utiliza para ver una colección de propiedades pertenecientes a otros objetos MAPI de un tipo determinado. Tablas MAPI se estructuran en un formato de fila y columna con cada fila que representa un objeto y cada columna que representa una propiedad del objeto. Una de las propiedades que normalmente se incluyen en cada fila es la propiedad de **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), un identificador que se puede usar para abrir y modificar el objeto. 
  
Debido a que las filas contienen valores de propiedad, la recuperación de una fila de una tabla es similar a obtener un conjunto de propiedades directamente desde el objeto que representa la fila. Ambas operaciones como resultado la recuperación de una matriz de valores de propiedad. La diferencia principal se encuentra en el control de durante cuánto tiempo propiedades de cadena y binarios. Para su inclusión en una tabla, algunos implementadores tabla truncan estas propiedades a 255 bytes. Al recuperar directamente desde el objeto, el valor completo siempre está disponible.
  
Las tablas se implementan por proveedores de almacén de libreta de direcciones y el mensaje de dirección y por MAPI, según el tipo de tabla y los objetos dentro de él. Un proveedor de almacén de mensajes implementa carpetas y una tabla de contenido para cada carpeta que incluye información acerca de los mensajes en la carpeta. Un proveedor de la libreta de direcciones implementa contenedores de la libreta de direcciones y una tabla de jerarquía que se muestra su organización. MAPI implementa varias tablas diferentes, algunos para su uso por las aplicaciones cliente, algunas para su uso por los proveedores de servicios y otros para su uso por ambos. La tabla de estado es única en que MAPI proporciona en última instancia en la tabla, pero las filas se componen de valiosas de todos los tipos de proveedores de servicios además de MAPI. 
  
En la siguiente ilustración se muestra uno de los usos frecuentes de una tabla en MAPI: para mostrar el contenido de una carpeta. En la parte derecha es una presentación de dos mensajes como es posible que aparezcan en una aplicación de cliente de mensajería típica. La presentación contiene cuatro elementos de información acerca de cada mensaje: el remitente, el destinatario, el asunto y el texto del mensaje. Cada parte de la información corresponde a una propiedad del mensaje.
  
En la izquierda es una vista de la tabla de contenido que incluye estos dos mensajes. Mientras que en la tabla de contenido puede tener diez filas debido a que la carpeta tiene diez mensajes, con cada fila que contiene muchos más de tres columnas, esta vista determinada está limitada a sólo dos filas y tres columnas.
  
La siguiente tabla muestran las propiedades que componen el conjunto de columnas de la vista de tabla.
  
|**Propiedad**|**Descripción**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nombre del remitente  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Fecha y hora cuando se envió el mensaje  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Línea de asunto del mensaje  <br/> |
   
Tenga en cuenta que el conjunto de propiedades que se muestran en el mensaje no son los mismos que el conjunto de columnas que se muestran en la tabla. El implementador de la tabla, en este caso un mensaje de proveedor de almacén, un valor predeterminado de fuentes de conjunto de columnas en un orden predeterminado. El cliente puede modificar este conjunto de columnas, que solicita columnas adicionales o el rechazo predeterminadas y pida que solicitarse de una manera específica. El cliente también puede ordenar las filas, ordenarlas según el valor de una o más columnas.
  
**Uso de una tabla para mostrar contenido de carpetas**
  
![Uso de una tabla para mostrar el contenido de la carpeta] (media/amapi_54.gif "Uso de una tabla para mostrar el contenido de la carpeta")
  
Existen dos interfaces para trabajar con tablas:
  
- [IMAPITable: IUnknown](imapitableiunknown.md) proporciona a los clientes y proveedores de servicios de una vista de solo lectura de los datos subyacentes de la tabla, lo que les permite ver y cambiar sólo la presentación. Varios usuarios pueden tener acceso a los mismos datos al mismo tiempo que **IMAPITable**. **IMAPITable** se implementa por MAPI y por los proveedores de servicios. 
    
- [ITableData: IUnknown](itabledataiunknown.md) proporciona a los clientes y proveedores de servicios de acceso de lectura/escritura a los datos subyacentes de la tabla, lo que les permite realizar cambios permanentes. **IMAPITable** se implementa mediante MAPI y resultan de utilidad para los proveedores de servicios que tienen acceso a él mediante una llamada a la función [CreateTable](createtable.md) . La implementación de **ITableData** contiene todos los datos para la tabla y cualquier asociado restricciones en la memoria, lo que apropiadas para usar con tablas muy grandes. Restricciones de compuestos y operaciones complejas, como la categorización no son compatibles. 
    
## <a name="see-also"></a>Recursos adicionales

- [Conceptos MAPI](mapi-concepts.md)

