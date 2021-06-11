---
title: Tablas de proveedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2b81f4aebae692d28ed492df102d59ba34debf63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408974"
---
# <a name="provider-tables"></a>Tablas de proveedor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una tabla de proveedor contiene información sobre los proveedores de servicios. Hay dos tablas de proveedor diferentes, ambas implementadas por MAPI y usadas por los clientes. La primera tabla, a la que se tiene acceso mediante una llamada al método [IMsgServiceAdmin::GetProviderTable,](imsgserviceadmin-getprovidertable.md) contiene información sobre todos los proveedores del perfil actual. La segunda tabla, a la que se tiene acceso a través de [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), crea una tabla que almacena información sobre todos los proveedores de servicios de un servicio de mensajes.
  
Estas dos tablas tienen otra diferencia. La tabla de proveedor disponible a través de **IMsgServiceAdmin::GetProviderTable** contiene solo filas que representan proveedores de servicios, mientras que la tabla disponible a través de **IProviderAdmin::GetProviderTable** puede incluir filas que representan información adicional asociada con un proveedor de servicios. Esta información adicional se agrega al perfil con la palabra clave "Secciones" de MAPISVC.INF. Cuando un proveedor tiene secciones de perfil adicionales, almacena los valores **MAPIUID** para estas secciones en la propiedad **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** se guarda en la sección perfil de servicio de mensajes. 
  
Las siguientes propiedades son la columna necesaria establecida en ambos tipos de tablas de proveedor:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
La tabla de proveedor se puede usar para mostrar el orden de transporte actual o para cambiarlo. Para mostrar el orden actual, cree una restricción para recuperar solo las filas con la propiedad **PR_RESOURCE_TYPE** establecida en MAPI_TRANSPORT_PROVIDER. A **continuación, use PR_PROVIDER_ORDINAL** como clave de ordenación para ordenar la tabla y recuperar todas las filas con el método [IMAPITable::QueryRows](imapitable-queryrows.md) o la [función HrQueryAllRows.](hrqueryallrows.md) 
  
Para cambiar el orden de transporte, aplique la misma restricción y recupere las filas. A continuación, cree una matriz de valores a partir **PR_PROVIDER_UID** propiedad que representa los identificadores únicos de los proveedores de transporte. Cuando los identificadores estén en el orden deseado, pásenlos al método [IMsgServiceAdmin::MsgServiceTransportOrder.](imsgserviceadmin-msgservicetransportorder.md) 
  
Una vez que se haya puesto a disposición una tabla de proveedor, no reflejará los cambios posteriores, como la adición o eliminación de un proveedor.
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

