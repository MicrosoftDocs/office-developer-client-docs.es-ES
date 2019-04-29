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
ms.openlocfilehash: 3eb190069b43ea1960c3b6edf30a9e0b782d2c41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425179"
---
# <a name="status-table-and-status-objects"></a>Tabla de estado y objetos de estado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI proporciona una tabla con información sobre el estado del subsistema MAPI, la cola de MAPI, la libreta de direcciones o un proveedor de servicios determinado. Puede obtener acceso a esta tabla llamando a [IMAPISession:: GetStatusTable](imapisession-getstatustable.md).
  
Cada fila de la tabla de estado representa un objeto de estado implementado por MAPI o por un proveedor de servicios. Puede usar un objeto status para mostrar la hoja de propiedades configuración de un proveedor, para cambiar la contraseña de un proveedor, para cargar o descargar mensajes y para comunicarse con un proveedor de transporte determinado. 
  
Hay dos formas de tener acceso a un objeto status:
  
- A través de la tabla de estado
    
- Mediante el método **OpenStatusEntry** de un objeto de inicio de sesión 
    
Como los objetos de inicio de sesión no están disponibles para los clientes, debe usar la tabla estado para obtener acceso a objetos de estado. El método de la tabla de estado es indirecto y requiere unas pocas llamadas antes de que se abra el objeto status y se devuelva un puntero a su implementación de **IMAPIStatus** . 
  
 **Para usar la tabla de estado para abrir un objeto de estado**
  
1. Llame a **IMAPIStatus:: GetStatusTable** para recuperar un puntero de [IMAPITable](imapitableiunknown.md) . 
    
2. Llame al método [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la tabla de estado para limitar la columna **** establecida como valor máximo ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) y **PR_DISPLAY_NAME** ([ PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
3. Limitar la vista de tabla a un objeto status determinado. Para las implementaciones de MAPI, un cliente puede definir una restricción de propiedad mediante **PR_RESOURCE_TYPE**. Para las implementaciones de proveedores de servicios, un cliente puede restringir en **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), el nombre del proveedor o en **PR_PROVIDER_DLL_NAME** ([PIDTAGPROVIDERDLLNAME](pidtagproviderdllname-canonical-property.md)), el nombre de la dll del proveedor. archivo.
    
4. Llame al [IMAPITable:: Restrict](imapitable-restrict.md) para establecer la restricción. 
    
5. Llame a [HrQueryAllRows](hrqueryallrows.md), pasando la estructura [SPropertyRestriction](spropertyrestriction.md) , para recuperar la fila que representa el estado del proveedor. 
    
6. Llame a [IMAPISession:: OpenEntry](imapisession-openentry.md), especificando el identificador de entrada de la fila tabla de estado, para abrir el objeto status y recuperar un puntero **IMAPIStatus** . 
    
Para mostrar una hoja de propiedades, llame al método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) del objeto status del proveedor de destino. **SettingsDialog** muestra una hoja de propiedades para visualización y, en algunos casos, para cambiar las propiedades de configuración de un proveedor. 
  
Para comunicarse con un proveedor de transporte, llame al método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) del objeto status. **ValidateState** puede reconfigurar un proveedor de transporte, evitar que el proveedor muestre una interfaz de usuario y controlar una sesión que implica la descarga de encabezados de mensajes desde un servidor remoto, en función de las marcas que se pasen. Por ejemplo, para cancelar la descarga de encabezados remotos, pase la marca ABORT_XP_HEADER_OPERATION a **ValidateState**. Para conectarse o desconectarse del servidor remoto, pase FORCE_XP_CONNECT o FORCE_XP_DISCONNECT. Para volver a configurar el proveedor, pase CONFIG_CHANGED. 
  
Los clientes que implementan el envío o la recepción de mensajes a petición llaman a un proveedor de transporte o al método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) del administrador de trabajos en cola de MAPI. Puede pasar tres marcas al método: FLUSH_UPLOAD, FLUSH_DOWNLOAD y FLUSH_FORCE. FLUSH_UPLOAD instruye al proveedor o a la cola MAPI para que envíe los mensajes en espera en la cola de salida mientras FLUSH_DOWNLOAD indica al proveedor o a la cola MAPI que recibirá los mensajes entrantes. FLUSH_FORCE puede establecerse con cualquiera de los demás indicadores para hacer que el objeto status realice el vaciado independientemente de la temporización. 
  
No espere poder llamar a **SettingsDialog** o [ChangePassword](imapistatus-changepassword.md) en ninguno de los objetos del subsistema MAPI, de la cola MAPI o del estado de la libreta de direcciones. Los objetos de estado de la libreta de direcciones y SUBSISTEMA solo admiten **ValidateState**; el objeto de estado de cola MAPI admite **FlushQueues** además de **ValidateState**.
  
## <a name="see-also"></a>Ver también



[Tablas de estado](status-tables.md)
  
[Objetos de estado MAPI](mapi-status-objects.md)

