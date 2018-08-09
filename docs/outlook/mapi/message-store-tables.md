---
title: Tablas de almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cdb7d8c5-8e35-47ff-8be7-2cb17e341ad3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 84631ea6d332829430bf9d99488f8a1a5fdebac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818403"
---
# <a name="message-store-tables"></a>Tablas de almacén de mensajes

  
  
**Hace referencia a**: Outlook 
  
En la tabla de almacenamiento de mensaje contiene información acerca de los proveedores de almacén de mensajes en el perfil actual. Hay una tabla de almacenamiento de mensajes para cada sesión MAPI, implementada por MAPI y utilizada por los clientes. Los clientes pueden utilizar esta tabla, por ejemplo, para buscar todas las instancias de un proveedor concreto o para localizar un almacén de mensajes específicos. 
  
La tabla de almacén de mensajes es dinámica. Si el usuario de una aplicación cliente edita el perfil, cambiar el almacén de mensajes de forma predeterminada, por ejemplo, los valores de la **PR_DEFAULT_STORE** las propiedades de los almacenes de mensaje afectado se actualizan inmediatamente. 
  
Los clientes de acceso a la tabla de almacenamiento de mensaje llamando al método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
Las siguientes propiedades que conforman la columna necesaria establecida en la tabla de almacén de mensajes:
  
|||
|:-----|:-----|
|**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**Entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Vea también



[Tablas MAPI](mapi-tables.md)

