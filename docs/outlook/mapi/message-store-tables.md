---
title: Tablas del almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dd28c146f6b05b2dea03f73fab7131f23ca99e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405355"
---
# <a name="message-store-tables"></a>Tablas del almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La tabla del almacén de mensajes contiene información acerca de los proveedores de al almacenamiento de mensajes en el perfil actual. Hay una tabla de almacenamiento de mensajes para cada sesión MAPI, implementada por MAPI y usada por los clientes. Los clientes pueden usar esta tabla, por ejemplo, para buscar todas las instancias de un proveedor determinado o para localizar un almacén de mensajes específico. 
  
La tabla del almacén de mensajes es dinámica. Si el usuario de una aplicación cliente edita el perfil, cambiando el almacén de mensajes predeterminado, por ejemplo, los valores de las propiedades **PR_DEFAULT_STORE** de los almacenes de mensajes afectados se actualizan inmediatamente. 
  
Los clientes tienen acceso a la tabla del almacén de mensajes llamando al [método IMAPISession::GetMsgStoresTable.](imapisession-getmsgstorestable.md) 
  
Las siguientes propiedades son la columna necesaria establecida en la tabla del almacén de mensajes:
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Consulte también



[Tablas MAPI](mapi-tables.md)

