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
ms.openlocfilehash: 36456c6226b2eb74b8f15995ad0925381302523a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820899"
---
# <a name="types-of-tables"></a>Tipos de tablas

  
  
**Hace referencia a**: Outlook 
  
Existen muchos tipos diferentes de las tablas, cada tipo diferenciado por la información que presenta. Tablas de habilitar las aplicaciones cliente y proveedores de servicios para obtener acceso fácilmente y manipular las propiedades importantes de muchos tipos de objetos. 
  
Algunas tablas, como las tablas de contenido, proporcionan una manera alternativa de obtener acceso a las propiedades. Por ejemplo, un cliente puede recuperar el asunto de un mensaje, su propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), ya sea directamente desde el mensaje mediante una llamada a su método [IMAPIProp::GetProps](imapiprop-getprops.md) o a través de la tabla de contenido del mensaje. Otras tablas proporcionan la única forma de obtener acceso a propiedades del objeto. Por ejemplo, un cliente no puede obtener acceso (propiedad) de un documento adjunto **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) mediante una llamada a **IMAPIProp::GetProps**; siempre debe recuperar la tabla de datos adjuntos del mensaje al que se adjunta. **PR_ATTACH_METHOD** es una columna necesaria en todas las tablas de datos adjuntos. 
  
Una vista de tabla puede ser dinámico o estático. Con una vista de tabla estática, los cambios realizados en los datos subyacentes hacen que la vista que se va a actualizarse. Una vez que se ha creado una instancia de la vista, no cambia. Los usuarios de tablas estáticas pueden estar informados de los cambios realizados en los datos a través de notificaciones de tabla. Una vista de tabla dinámica se actualiza cuando se realizan cambios en los datos. Hay dos tipos de tablas dinámicas: uno que actualiza las columnas de cada fila, pero las filas permanecen estáticos y que actualiza las filas y columnas. Este último tipo de tabla siempre refleja exactamente los datos subyacentes.
  
Las tablas tienen una columna predeterminado establecido, el conjunto mínimo de columnas que puede esperar un proveedor de servicio o cliente para ver cuando llame al recuperar filas de una tabla que aún no se ha afectado por un [IMAPITable::SetColumns](imapitable-setcolumns.md) . Los clientes y proveedores de servicios pueden agregar columnas a o quitar columnas de este valor predeterminado que se establece mediante una llamada mediante el método **SetColumns** . Los cambios pueden estar estática o dinámicamente, siguiendo una solicitud de cliente. No todas las tablas admiten la modificación del conjunto de columna dinámica. 
  
Las tablas MAPI y sus implementadores y los usuarios son:
  
|**Table**|**Implementadores**|
|:-----|:-----|
|Datos adjuntos  <br/> |Implementada por los proveedores de almacén de mensajes. Usada por los clientes y los proveedores de transporte.  <br/> |
|Contenido  <br/> |Implementado por mensaje almacenar y los proveedores de libreta de direcciones. Utilizado por los clientes.  <br/> |
|Visualización  <br/> |Implementado por MAPI y los proveedores de servicios. Usado por MAPI y los proveedores de servicios.  <br/> |
|Jerarquía  <br/> |Implementado por mensaje almacenar y los proveedores de libreta de direcciones. Utilizado por los clientes.  <br/> |
|Servicio de mensajes  <br/> |Se implementa mediante MAPI. Utilizado por los clientes.  <br/> |
|Almacén de mensajes  <br/> |Se implementa mediante MAPI. Utilizado por los clientes.  <br/> |
|Uso único  <br/> |Implementada por los proveedores de la libreta de direcciones. Usada por MAPI.  <br/> |
|Cola de salida  <br/> |Implementada por los proveedores de almacén de mensajes. Usada por la cola de MAPI.  <br/> |
|Perfil  <br/> |Se implementa mediante MAPI. Utilizado por los clientes.  <br/> |
|Proveedor  <br/> |Se implementa mediante MAPI. Utilizado por los clientes.  <br/> |
|Carpeta de recepci�n  <br/> |Implementada por los proveedores de almacén de mensajes. Utilizado por los clientes.  <br/> |
|Recipient  <br/> |Implementada por los proveedores de almacén de mensajes. Usada por los clientes y los proveedores de transporte.  <br/> |
|Status  <br/> |Implementado por MAPI y los proveedores de servicios. Utilizado por los clientes.  <br/> |
   
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

