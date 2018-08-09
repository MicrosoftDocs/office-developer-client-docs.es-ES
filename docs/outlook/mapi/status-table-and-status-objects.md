---
title: Tabla de estado y objetos de estado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 774aaea0365066981b9d6426a2579160f6578844
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820762"
---
# <a name="status-table-and-status-objects"></a>Tabla de estado y objetos de estado

  
  
**Hace referencia a**: Outlook 
  
MAPI proporciona una tabla con información sobre el estado del subsistema MAPI, cola MAPI, la libreta de direcciones o un proveedor de servicio en particular. Puede tener acceso a esta tabla mediante una llamada a [IMAPISession::GetStatusTable](imapisession-getstatustable.md).
  
Cada fila de la tabla de estado representa un objeto de estado que se implementa mediante MAPI o un proveedor de servicios. Puede usar un objeto de estado para mostrar la hoja de propiedades de configuración de un proveedor, para cambiar la contraseña de un proveedor, para cargar o descargar los mensajes y para comunicarse con un proveedor de transporte concreto. 
  
Existen dos maneras de obtener acceso a un objeto de estado:
  
- A través de la tabla de estado
    
- A través del método de **OpenStatusEntry** del objeto de inicio de sesión 
    
Debido a que los objetos de inicio de sesión no están disponibles para los clientes, debe usar la tabla de estado para tener acceso a objetos de estado. El enfoque de la tabla de estado es indirecto, que requieren algunas llamadas antes de que se abre el objeto de estado y devuelve un puntero a su implementación **IMAPIStatus** . 
  
 **Para usar la tabla de estado para abrir un objeto de estado**
  
1. Llame a **IMAPIStatus::GetStatusTable** para recuperar un puntero [IMAPITable](imapitableiunknown.md) . 
    
2. Llamar al método [IMAPITable::SetColumns](imapitable-setcolumns.md) de la tabla de estado para limitar la columna establecida en la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) y **PR_DISPLAY_NAME** ([ PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
3. Limitar la vista de tabla a un objeto de estado en particular. Para las implementaciones de MAPI, un cliente puede definir una restricción de propiedad con **PR_RESOURCE_TYPE**. Para las implementaciones del proveedor de servicio, un cliente puede restringir en **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), el nombre del proveedor, o en **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)), el nombre del proveedor del archivo DLL archivo.
    
4. Llamar a [IMAPITable:: Restrict](imapitable-restrict.md) para establecer la restricción. 
    
5. Llame a [HrQueryAllRows](hrqueryallrows.md), pasando la estructura [SPropertyRestriction](spropertyrestriction.md) , para recuperar la fila que representa el estado del proveedor. 
    
6. Llame a [IMAPISession::OpenEntry](imapisession-openentry.md), que especifica el identificador de entrada de la fila de tabla de estado para abrir el objeto de estado y recuperar un puntero **IMAPIStatus** . 
    
Para mostrar una hoja de propiedades, llamar al método [SettingsDialog](imapistatus-settingsdialog.md) del objeto de estado para el proveedor de destino. **Diálogo Configuración** muestra una hoja de propiedades para su visualización y en algunos casos, cambiar las propiedades de un proveedor de configuración. 
  
Para comunicarse con un proveedor de transporte, llame al método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) del objeto de su estado. Puede volver a configurar un proveedor de transporte, evitar que el proveedor muestre una interfaz de usuario y controlar una sesión que implica la descarga de encabezados de los mensajes desde un servidor remoto, dependiendo de los indicadores que pasan en **ValidateState** . Por ejemplo, para cancelar la descarga de encabezados remotos, pase el indicador ABORT_XP_HEADER_OPERATION a **ValidateState**. Para conectarse o desconectarse del servidor remoto, pase FORCE_XP_CONNECT o FORCE_XP_DISCONNECT. Para volver a configurar el proveedor, pase CONFIG_CHANGED. 
  
Los clientes que implementan el envío o recepción de mensajes a petición llame al método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) de un proveedor de transporte o en la cola MAPI. Puede pasar tres indicadores en el método: FLUSH_UPLOAD, FLUSH_DOWNLOAD y FLUSH_FORCE. FLUSH_UPLOAD indica que el proveedor o la cola MAPI para enviar todos los mensajes en espera en la cola de salida mientras FLUSH_DOWNLOAD indica al proveedor o la cola MAPI para recibir los mensajes entrantes. FLUSH_FORCE se puede establecer con cualquiera de los otros marcadores para hacer que el objeto de estado realizar el vaciado independientemente el momento oportuno. 
  
No se espera que puedan llamar al **diálogo Configuración** o [ChangePassword](imapistatus-changepassword.md) en cualquiera de los subsistema MAPI, la cola MAPI o la dirección de objetos de estado de la libreta. Los objetos de estado de la libreta del subsistema y la dirección solo admiten **ValidateState**; el objeto de estado de cola de impresión MAPI admite **FlushQueues** además de **ValidateState**.
  
## <a name="see-also"></a>Vea también



[Tablas de estado](status-tables.md)
  
[Objetos de estado MAPI](mapi-status-objects.md)

