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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336466"
---
# <a name="status-tables"></a>Tablas de estado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La tabla de estado contiene información sobre el estado de la sesión actual. Hay una tabla de estado para cada sesión MAPI que incluye información proporcionada por MAPI y por proveedores de servicios. MAPI proporciona datos para tres filas: una fila para el subsistema MAPI, una fila para la cola MAPI y una fila para la libreta de direcciones integrada. Como los proveedores de transporte deben suministrar información de estado a la tabla de estado, hay una fila por cada proveedor de transporte activo. La libreta de direcciones y los proveedores de almacenamiento de mensajes pueden elegir si admiten la tabla de estado. 
  
Debido a que cada fila la proporciona un recurso diferente, el conjunto de columnas puede variar de una fila a otra. Hay un conjunto de columnas que cada objeto de Estado debe proporcionar y un conjunto de columnas que proporciona MAPI. Un proveedor de servicios puede Agregar a estos conjuntos para exponer propiedades específicas del proveedor. Por ejemplo, los proveedores de almacenamiento de mensajes podrían agregar **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) para proporcionar a los clientes el identificador de su almacén de mensajes. Los clientes deben tener un conocimiento avanzado de la existencia de esta información adicional para poder usarla. 
  
En la siguiente tabla se enumeran las propiedades que deben estar en cada fila de la tabla de estado. El implementador del objeto status proporciona algunas de las propiedades; otros son calculados por MAPI.
  
|**Propiedades proporcionadas por el objeto status**|**Propiedades proporcionadas por MAPI**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
Si el objeto status proporciona una identidad, debe establecer **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)), **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) y **PR_IDENTITY_SEARCH_KEY** ([ PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) e incluya estas propiedades en la tabla. 
  
MAPI calcula cuatro propiedades para cada fila de la tabla de estado:
  
|||
|:-----|:-----|
|**** Es ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI asigna un identificador de entrada a la fila de estado para permitir a los clientes abrir el objeto de estado correspondiente. Un identificador de fila también se asigna para identificar la fila de la tabla, como una clave de instancia para identificar los datos en el objeto de estado. La propiedad **PR_OBJECT_TYPE** se establece en MAPI_STATUS. 
  
Para tener acceso a la tabla de estado, los clientes llaman al método [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) . Esta llamada no debe realizarse inmediatamente al iniciarse. Esto se debe a que **GetStatusTable** tiene que esperar a que la cola MAPI inicialice los proveedores de transporte, una operación que se pospone hasta que el cliente haya finalizado el inicio de sesión. **GetStatusTable** es una llamada relativamente rápida después de que la cola MAPI haya finalizado el procesamiento de inicio. 
  
La información de la tabla de estado puede usarse de varias formas, por ejemplo, para tener acceso a un objeto de estado, para determinar si un cliente se está ejecutando en modo conectado o sin conexión, y para supervisar el estado de un proveedor. Por ejemplo, los clientes pueden abrir un objeto de estado de un proveedor de servicios específico pasando el **** valor de la propiedad del método [IMAPISession:: OpenEntry](imapisession-openentry.md) . El objeto status admite la interfaz **IMAPIStatus** , una interfaz que contiene métodos para cambiar una contraseña del proveedor de servicios, vaciar la cola de mensajes, mostrar una hoja de propiedades de configuración o confirmar el estado de un proveedor directamente. La información de la tabla de estado también se puede usar para crear un cuadro de diálogo que informe a los clientes del progreso durante una operación de larga duración. 
  
Los proveedores de servicios que admiten la tabla de estado usan el método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) para crear y actualizar su fila. Siempre que se produce un cambio en su fila, se deben notificar todos los objetos del receptor de notificaciones registrados para recibir notificaciones de tabla de estado. Los proveedores de servicios pueden llamar al método [IMAPISupport:: Notify](imapisupport-notify.md) si usan la utilidad de notificación MAPI o llamar directamente al método [IMAPIAdviseSink:: NotifyTo](imapiadvisesink-onnotify.md) de cada receptor de notificaciones. 
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

