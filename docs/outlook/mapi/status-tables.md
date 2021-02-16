---
title: Tablas de estado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2b2aca7-757f-4260-96a5-d0af55189711
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d612738ef8bf0e6925d89a5be7cb423695672d28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422365"
---
# <a name="status-tables"></a>Tablas de estado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La tabla de estado contiene información relacionada con el estado de la sesión actual. Hay una tabla de estado para cada sesión MAPI que incluye información proporcionada por MAPI y por proveedores de servicios. MAPI proporciona datos para tres filas: una fila para el subsistema MAPI, una fila para la cola MAPI y una fila para la libreta de direcciones integrada. Dado que los proveedores de transporte deben proporcionar información de estado a la tabla de estado, hay una fila para cada proveedor de transporte activo. Los proveedores de libreta de direcciones y almacén de mensajes pueden elegir si admiten la tabla de estado. 
  
Dado que cada fila la proporciona un recurso diferente, el conjunto de columnas puede variar de una fila a otra. Hay un conjunto de columnas que todos los objetos de estado deben suministrar y un conjunto de columnas que proporciona MAPI. Un proveedor de servicios puede agregar a estos conjuntos para exponer propiedades específicas del proveedor. Por ejemplo, los proveedores de almacén de mensajes pueden agregar **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) para proporcionar a los clientes el identificador de su almacén de mensajes. Los clientes deben tener conocimiento previo de la existencia de esta información adicional para poder usarla. 
  
En la tabla siguiente se enumeran las propiedades que deben estar en cada fila de tabla de estado. El implementador del objeto de estado proporciona algunas de las propiedades; Otros se calculan mediante MAPI.
  
|**Propiedades proporcionadas por el objeto de estado**|**Propiedades proporcionadas por MAPI**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
Si el objeto de estado proporciona una identidad, debe establecer **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)), **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) y **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) e incluir estas propiedades en la tabla. 
  
MAPI calcula cuatro propiedades para cada fila de tabla de estado:
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI asigna un identificador de entrada a la fila de estado para permitir que los clientes abran el objeto de estado correspondiente. También se asigna un identificador de fila para identificar la fila de la tabla como una clave de instancia para identificar los datos en el objeto de estado. La **PR_OBJECT_TYPE** propiedad está establecida en MAPI_STATUS. 
  
Para obtener acceso a la tabla de estado, los clientes llaman [al método IMAPISession::GetStatusTable.](imapisession-getstatustable.md) Esta llamada no debe realizarse inmediatamente al iniciarse. Esto se debe a **que GetStatusTable** tiene que esperar a que la cola MAPI inicialice los proveedores de transporte, una operación que se pospone hasta después de que el cliente haya terminado de iniciar sesión. **GetStatusTable es** una llamada relativamente rápida después de que la cola MAPI haya completado su procesamiento de inicio. 
  
La información de la tabla de estado se puede usar de varias maneras, como para obtener acceso a un objeto de estado, para determinar si un cliente se ejecuta en un modo conectado o sin conexión, y para supervisar el estado de un proveedor. Por ejemplo, los clientes pueden abrir el objeto de estado de un proveedor de servicios específico pasando el valor de la propiedad **PR_ENTRYID** al método [IMAPISession::OpenEntry.](imapisession-openentry.md) El objeto de estado admite la interfaz **IMAPIStatus,** una interfaz que contiene métodos para cambiar una contraseña del proveedor de servicios, vaciar la cola de mensajes, mostrar una hoja de propiedades de configuración o confirmar el estado con un proveedor directamente. La información de la tabla de estado también se puede usar para crear un cuadro de diálogo para informar a los clientes del progreso durante una operación larga. 
  
Los proveedores de servicios que admiten la tabla de estado usan el método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para crear y actualizar su fila. Siempre que se produzca un cambio en su fila, todos los objetos receptores de aviso registrados para recibir notificaciones de la tabla de estado deben recibir una notificación. Los proveedores de servicios pueden llamar al método [IMAPISupport::Notify](imapisupport-notify.md) si usan la utilidad de notificación MAPI o llamar directamente al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de cada receptor de avisos. 
  
## <a name="see-also"></a>Consulte también



[Tablas MAPI](mapi-tables.md)

