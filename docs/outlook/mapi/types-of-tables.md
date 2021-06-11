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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426467"
---
# <a name="types-of-tables"></a>Tipos de tablas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay muchos tipos diferentes de tablas, cada tipo diferenciado por la información que presenta. Las tablas permiten que las aplicaciones cliente y los proveedores de servicios puedan acceder y manipular fácilmente las propiedades importantes de muchos tipos de objetos. 
  
Algunas tablas, como las tablas de contenido, proporcionan una forma alternativa de obtener acceso a las propiedades. Por ejemplo, un cliente puede recuperar el asunto de un mensaje ( su propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) directamente desde el mensaje llamando a su método [IMAPIProp::GetProps](imapiprop-getprops.md) o a través de la tabla de contenido del mensaje. Otras tablas proporcionan la única forma de obtener acceso a las propiedades del objeto. Por ejemplo, un cliente no puede tener acceso a la propiedad PR_ATTACH_METHOD **(** [PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) llamando a **IMAPIProp::GetProps**; siempre debe recuperar la tabla de datos adjuntos del mensaje al que está adjunta. **PR_ATTACH_METHOD** es una columna obligatoria en todas las tablas de datos adjuntos. 
  
Una vista de tabla puede ser estática o dinámica. Con una vista de tabla estática, los cambios en los datos subyacentes no hacen que se actualice la vista. Una vez que se crea una instancia de la vista, no cambia. Los usuarios de tablas estáticas pueden estar informados de los cambios realizados en los datos a través de notificaciones de tabla. Una vista de tabla dinámica se actualiza cuando se realizan cambios en los datos. Hay dos tipos de tablas dinámicas: una que actualiza las columnas de cada fila, pero las filas permanecen estáticas y otra que actualiza las columnas y las filas. Este último tipo de tabla siempre refleja exactamente los datos subyacentes.
  
Las tablas tienen un conjunto de columnas predeterminado, el conjunto mínimo de columnas que un cliente o proveedor de servicios puede esperar ver al recuperar filas de una tabla que aún no se ha visto afectada por una llamada [IMAPITable::SetColumns.](imapitable-setcolumns.md) Los clientes y proveedores de servicios pueden agregar columnas a o quitar columnas de este conjunto predeterminado llamando al **método SetColumns.** Los cambios se pueden realizar de forma estática o dinámica, después de una solicitud de cliente. No todas las tablas admiten la modificación del conjunto dinámico de columnas. 
  
Las tablas MAPI y sus implementadores y usuarios son:
  
|**Table**|**Implementadores**|
|:-----|:-----|
|Datos adjuntos  <br/> |Implementado por proveedores de almacén de mensajes. Usado por clientes y proveedores de transporte.  <br/> |
|Contenido  <br/> |Implementado por proveedores de almacén de mensajes y libreta de direcciones. Usado por los clientes.  <br/> |
|Pantalla  <br/> |Implementado por MAPI y proveedores de servicios. Usado por MAPI y los proveedores de servicios.  <br/> |
|Hierarchy  <br/> |Implementado por proveedores de almacén de mensajes y libreta de direcciones. Usado por los clientes.  <br/> |
|Servicio de mensajes  <br/> |Implementado por MAPI. Usado por los clientes.  <br/> |
|Almacén de mensajes  <br/> |Implementado por MAPI. Usado por los clientes.  <br/> |
|One-off  <br/> |Implementado por proveedores de libreta de direcciones. Se usa por MAPI.  <br/> |
|Cola saliente  <br/> |Implementado por proveedores de almacén de mensajes. Usado por la cola MAPI.  <br/> |
|Perfil  <br/> |Implementado por MAPI. Usado por los clientes.  <br/> |
|Proveedor  <br/> |Implementado por MAPI. Usado por los clientes.  <br/> |
|Carpeta de recepci�n  <br/> |Implementado por proveedores de almacén de mensajes. Usado por los clientes.  <br/> |
|Destinatario  <br/> |Implementado por proveedores de almacén de mensajes. Usado por clientes y proveedores de transporte.  <br/> |
|Estado  <br/> |Implementado por MAPI y proveedores de servicios. Usado por los clientes.  <br/> |
   
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

