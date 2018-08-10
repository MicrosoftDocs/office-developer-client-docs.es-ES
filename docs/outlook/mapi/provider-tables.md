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
ms.openlocfilehash: a613bd744a113b4378c5bef94fb51f6ae3aa4041
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820461"
---
# <a name="provider-tables"></a>Tablas de proveedor

  
  
**Hace referencia a**: Outlook 
  
Una tabla de proveedor contiene información acerca de los proveedores de servicio. Hay dos tablas de otro proveedor, ambos implementan por MAPI y utilizan por los clientes. La primera tabla, tener acceso a llamando al método [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) , contiene información acerca de todos los proveedores para el perfil actual. La segunda tabla, tiene acceso a través de [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), crea una tabla que almacena información acerca de todos los proveedores de servicios para un servicio de mensajes.
  
Estas dos tablas tienen otra diferencia. En la tabla de proveedor disponible a través de **IMsgServiceAdmin::GetProviderTable** contiene sólo las filas que representan los proveedores de servicios, mientras que la tabla disponible a través de **IProviderAdmin::GetProviderTable** puede incluir filas que representan información adicional asociada a un proveedor de servicios. Esta información adicional se agrega al perfil con la palabra clave "Secciones" de MAPISVC.INF. Cuando un proveedor tiene secciones de perfil adicional, almacena los valores **MAPIUID** de estas secciones en la propiedad **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** se guarda en la sección de perfil de servicio de mensaje. 
  
Las siguientes propiedades que conforman la columna requiere establecer en ambos tipos de tablas de proveedor:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
En la tabla de proveedor se puede usar para mostrar el orden de transporte actual o para cambiarlo. Para mostrar el orden actual, crear una restricción para recuperar sólo las filas con la propiedad **PR_RESOURCE_TYPE** establecida en MAPI_TRANSPORT_PROVIDER. A continuación, use **PR_PROVIDER_ORDINAL** como criterio de ordenación para ordenar la tabla y recuperar todas las filas con el método [IMAPITable:: QueryRows](imapitable-queryrows.md) o la función [HrQueryAllRows](hrqueryallrows.md) . 
  
Para cambiar el orden de transporte, aplicar la misma restricción y recuperar las filas. A continuación, cree una matriz de valores de la propiedad **PR_PROVIDER_UID** que representa los identificadores únicos para los proveedores de transporte. Cuando los identificadores se encuentran en el orden deseado, pase al método [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) . 
  
Después de que se ha realizado una tabla de proveedor disponible, no reflejarán los cambios posteriores, como la adición o eliminación de un proveedor.
  
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

