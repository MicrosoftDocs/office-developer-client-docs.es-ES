---
title: Tipos de tablas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1fc4f20-511f-4721-8f09-ec2a5fd0ccb0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 732b3d724c855d978250afff3d05c7f19909a5b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356577"
---
# <a name="types-of-tables"></a>Tipos de tablas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay muchos tipos diferentes de tablas, cada tipo que se diferencian por la información que presenta. Las tablas permiten a las aplicaciones cliente y a los proveedores de servicios tener acceso y manipular fácilmente las propiedades importantes de muchos tipos de objetos. 
  
Algunas tablas, como las tablas de contenido, proporcionan una forma alternativa de obtener acceso a las propiedades. Por ejemplo, un cliente puede recuperar el asunto de un mensaje, su propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), directamente desde el mensaje llamando a su método [IMAPIProp:: GetProps](imapiprop-getprops.md) o a través de la tabla de contenido del mensaje. Otras tablas proporcionan la única forma de tener acceso a las propiedades de los objetos. Por ejemplo, un cliente no puede obtener acceso a la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) de datos adjuntos llamando a **IMAPIProp:: GetProps**; siempre debe recuperar la tabla de datos adjuntos del mensaje al que está adjunta. **PR_ATTACH_METHOD** es una columna obligatoria en todas las tablas de datos adjuntos. 
  
Una vista de tabla puede ser estática o dinámica. Con una vista de tabla estática, los cambios realizados en los datos subyacentes no provocan la actualización de la vista. Una vez que se ha creado una instancia de la vista, no cambia. Se puede informar a los usuarios de tablas estáticas de los cambios en los datos a través de las notificaciones de tabla. Una vista de tabla dinámica se actualiza cuando se realizan cambios en los datos. Hay dos tipos de tablas dinámicas: una que actualiza las columnas de cada fila, pero las filas permanecen estáticas y otra que actualiza las columnas y las filas. Este último tipo de tabla siempre refleja exactamente los datos subyacentes.
  
Las tablas tienen un conjunto de columnas predeterminado, el conjunto mínimo de columnas que un cliente o proveedor de servicios puede esperar ver al recuperar filas de una tabla que todavía no se han visto afectadas por una llamada [IMAPITable:: SetColumns](imapitable-setcolumns.md) . Los clientes y los proveedores de servicios pueden agregar o quitar columnas de este conjunto predeterminado llamando al método **SetColumns** . Los cambios se pueden realizar de forma estática o dinámica siguiendo una solicitud de cliente. No todas las tablas admiten la modificación del conjunto de columnas dinámicas. 
  
Las tablas MAPI y los implementadores y usuarios son los siguientes:
  
|**Table**|**Los implementadores**|
|:-----|:-----|
|Datos adjuntos  <br/> |Lo implementan los proveedores de almacenamiento de mensajes. Lo usan los clientes y los proveedores de transporte.  <br/> |
|Contenido  <br/> |Implementado por los proveedores de almacenamiento de mensajes y libreta de direcciones. Usada por los clientes.  <br/> |
|Visualización  <br/> |Lo implementan los proveedores de servicios y MAPI. Lo usan los proveedores de servicios y MAPI.  <br/> |
|Hierarchy  <br/> |Implementado por los proveedores de almacenamiento de mensajes y libreta de direcciones. Usada por los clientes.  <br/> |
|Servicio de mensajes  <br/> |Implementada por MAPI. Usada por los clientes.  <br/> |
|Almacén de mensajes  <br/> |Implementada por MAPI. Usada por los clientes.  <br/> |
|Uso único  <br/> |Lo implementan los proveedores de libreta de direcciones. Usada por MAPI.  <br/> |
|Cola de salida  <br/> |Lo implementan los proveedores de almacenamiento de mensajes. Usada por la cola MAPI.  <br/> |
|Perfil  <br/> |Implementada por MAPI. Usada por los clientes.  <br/> |
|Proveedor  <br/> |Implementada por MAPI. Usada por los clientes.  <br/> |
|Carpeta de recepci�n  <br/> |Lo implementan los proveedores de almacenamiento de mensajes. Usada por los clientes.  <br/> |
|Recipient  <br/> |Lo implementan los proveedores de almacenamiento de mensajes. Lo usan los clientes y los proveedores de transporte.  <br/> |
|Estado  <br/> |Lo implementan los proveedores de servicios y MAPI. Usada por los clientes.  <br/> |
   
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

