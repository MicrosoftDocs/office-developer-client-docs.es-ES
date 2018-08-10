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
ms.openlocfilehash: afbef333af46051284fa51d52c2e3f77607b0b13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820770"
---
# <a name="status-tables"></a>Tablas de estado

  
  
**Hace referencia a**: Outlook 
  
La tabla de estado contiene información relacionada con el estado de la sesión actual. Hay una tabla de estado para cada sesión MAPI que incluye la información proporcionada por MAPI y por los proveedores de servicios. MAPI proporciona datos para tres filas: una fila para el subsistema MAPI, una fila de la cola MAPI y una fila de la libreta de direcciones integrada. Debido a que los proveedores de transporte son necesarios para suministrar información de estado a la tabla de estado, no hay una fila por cada proveedor de transporte activa. Proveedores de almacén de libreta de direcciones y el mensaje de dirección pueden elegir si desea admitir la tabla de estado. 
  
Debido a que cada fila es proporcionado por un recurso diferente, el conjunto de columnas puede variar en cada fila. Hay un conjunto de columnas que se requiere para proporcionar cada objeto de estado y un conjunto de columnas que suministran los MAPI. Puede agregar un proveedor de servicios a estos conjuntos para exponer propiedades específicas del proveedor. Por ejemplo, los proveedores de almacén de mensajes es posible que agregue **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) para proporcionar a los clientes con el identificador de su almacén de mensajes. Los clientes deben tener conocimiento anticipado de la existencia de esta información adicional para poder usarla. 
  
En la siguiente tabla se enumera las propiedades que deben estar en cada fila de la tabla de estado. El implementador del objeto status proporciona algunas de las propiedades; otros usuarios se calculan por MAPI.
  
|**Propiedades proporcionadas por el objeto de estado**|**Propiedades de MAPI**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
Si el objeto de estado proporciona una identidad, se deben establecer **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)), **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) y **PR_IDENTITY_SEARCH_KEY** ([ PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) e incluya estas propiedades en la tabla. 
  
Se calculan cuatro propiedades MAPI para cada fila de la tabla de estado:
  
|||
|:-----|:-----|
|**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI asigna un identificador de entrada a la fila de estado para que los clientes puedan abrir el objeto de estado correspondiente. También se asigna un identificador de fila para identificar la fila en la tabla como es una clave de instancia para identificar los datos en el objeto de estado. La propiedad **PR_OBJECT_TYPE** se establece en MAPI_STATUS. 
  
Para obtener acceso a la tabla de estado, los clientes de llaman al método [IMAPISession::GetStatusTable](imapisession-getstatustable.md) . Esta llamada no debe realizarse inmediatamente tras el inicio. Esto es debido a que **GetStatusTable** tiene que esperar la cola MAPI inicializar los proveedores de transporte, una operación que se pospuso hasta después de que el cliente ha terminado de su inicio de sesión. **GetStatusTable** es una llamada relativamente rápida después de la cola MAPI ha completado el procesamiento de inicio. 
  
Información de la tabla de estado puede usarse en una variedad de formas, como por ejemplo, para tener acceso a un objeto de estado, para determinar si un cliente se está ejecutando en un modo conectado o sin conexión y para supervisar el estado de un proveedor. Por ejemplo, los clientes pueden abrir el objeto de estado de un determinado proveedor de servicios pasando el valor de la propiedad de **entrada del objeto** al método [IMAPISession::OpenEntry](imapisession-openentry.md) . El objeto de estado es compatible con la interfaz **IMAPIStatus** , una interfaz que contiene los métodos para cambiar la contraseña de un proveedor de servicios, vaciar la cola de mensajes, mostrar una hoja de propiedades de configuración o comprobar el estado de directamente con un proveedor. Información de la tabla de estado también puede usarse para crear un cuadro de diálogo para informar a los clientes de progreso durante una operación prolongada. 
  
Proveedores de servicios que son compatibles con la tabla de estado de usar el método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para crear y actualizar su fila. Cada vez que se produce un cambio en su fila, todos de aviso deben recibir una notificación de objetos del receptor registrados para recibir notificaciones de estado de tabla. Proveedores de servicios pueden llamar al método de [IMAPISupport::Notify](imapisupport-notify.md) si está usando la utilidad de notificación de MAPI o llamar directamente al método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de cada receptor de notificaciones. 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

