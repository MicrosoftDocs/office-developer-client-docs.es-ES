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
ms.openlocfilehash: 840c34a64cd0478be8f208799653b9916f50079d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437087"
---
# <a name="mapi-tables"></a>Tablas MAPI
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla MAPI es un objeto MAPI que se usa para ver una colección de propiedades pertenecientes a otros objetos MAPI de un tipo determinado. Las tablas MAPI se estructuran en un formato de fila y columna con cada fila que representa un objeto y cada columna que representa una propiedad del objeto. Una de las propiedades que normalmente se incluyen en cada fila es la propiedad **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), un identificador que se puede usar para abrir y modificar el objeto. 
  
Dado que las filas contienen valores de propiedad, recuperar una fila de una tabla es similar a obtener un conjunto de propiedades directamente desde el objeto que representa la fila. Ambas operaciones resultan en la recuperación de una matriz de valores de propiedad. La diferencia principal está en el control de las propiedades de cadena larga y binaria. Para su inclusión en una tabla, algunos implementadores de tablas truncan estas propiedades en 255 bytes. Cuando se recupera directamente desde el objeto, el valor completo siempre está disponible.
  
Las tablas se implementan mediante proveedores de libreta de direcciones y almacén de mensajes y MAPI, según el tipo de tabla y los objetos que contiene. Un proveedor de almacén de mensajes implementa carpetas y una tabla de contenido para cada carpeta que incluye información sobre los mensajes de la carpeta. Un proveedor de libreta de direcciones implementa contenedores de libreta de direcciones y una tabla de jerarquía que muestra su organización. MAPI implementa varias tablas diferentes, algunas para su uso por aplicaciones cliente, otras para su uso por los proveedores de servicios y otras para su uso por ambas. La tabla de estado es única en que MAPI suministra finalmente la tabla, pero las filas se componen de contribuciones de todos los tipos de proveedores de servicios además de MAPI. 
  
En la siguiente ilustración se muestra uno de los usos frecuentes de una tabla en MAPI: para mostrar el contenido de una carpeta. A la derecha hay una presentación de dos mensajes como puede aparecer en una aplicación cliente de mensajería típica. La pantalla contiene cuatro partes de información sobre cada mensaje: el remitente, el destinatario, el asunto y el texto del mensaje. Cada fragmento de información corresponde a una propiedad del mensaje.
  
A la izquierda hay una vista de la tabla de contenido que incluye estos dos mensajes. Mientras que la tabla de contenido puede tener diez filas porque la carpeta tiene diez mensajes, con cada fila que contiene muchas más de tres columnas, esta vista en particular está limitada a solo dos filas y tres columnas.
  
En la tabla siguiente se muestran las propiedades que forma parte del conjunto de columnas de la vista de tabla.
  
|**Propiedad**|**Descripción**|
|:-----|:-----|
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nombre del remitente  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |Fecha y hora en que se envió el mensaje  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Línea de asunto del mensaje  <br/> |
   
Observe que el conjunto de propiedades que se muestra en el mensaje no es el mismo que el conjunto de columnas que se muestran en la tabla. El implementador de la tabla, en este caso un proveedor de almacén de mensajes, proporciona un conjunto predeterminado de columnas en un orden predeterminado. El cliente puede modificar este conjunto de columnas, solicitar columnas adicionales o rechazar las predeterminadas y solicitar que se ordenan de una forma específica. El cliente también puede ordenar las filas, ordenándolos según el valor de una o más columnas.
  
**Uso de una tabla para mostrar contenido de carpetas**
  
![Uso de una tabla para mostrar el contenido de la carpeta]Mediante una tabla para mostrar el contenido de la(media/amapi_54.gif "carpeta")
  
Hay dos interfaces para trabajar con tablas:
  
- [IMAPITable: IUnknown](imapitableiunknown.md) proporciona a los clientes y proveedores de servicios una vista de solo lectura de los datos subyacentes de la tabla, lo que les permite ver y cambiar solo la presentación. Varios usuarios pueden tener acceso a los mismos datos simultáneamente con **IMAPITable**. **IMAPITable lo** implementan MAPI y los proveedores de servicios. 
    
- [ITableData: IUnknown](itabledataiunknown.md) proporciona a los clientes y proveedores de servicios acceso de lectura y escritura a los datos subyacentes de la tabla, lo que les permite realizar cambios permanentes. **IMAPITable** se implementa mediante MAPI y lo usan principalmente los proveedores de servicios que tienen acceso a ella llamando a la [función CreateTable.](createtable.md) La **implementación de ITableData** contiene todos los datos de la tabla y las restricciones asociadas en la memoria, por lo que no es adecuado para su uso con tablas muy grandes. Las restricciones compuestas y las operaciones complejas como la categorización no son compatibles. 
    
## <a name="see-also"></a>Vea también

- [Conceptos de MAPI](mapi-concepts.md)

