---
title: Tablas de servicio de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 569c1bd7ee2f4ac6c321f234be2954a57715549b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576675"
---
# <a name="message-service-tables"></a>Tablas de servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La tabla de mensajes de servicio contiene información acerca de los servicios de mensaje en el perfil actual. Hay una tabla de servicio de mensaje para cada sesión MAPI, implementada por MAPI y usados por las aplicaciones de cliente de propósito especial que proporcionan compatibilidad con la configuración. 
  
La tabla de mensajes de servicio es una tabla estática.
  
Los clientes de acceso a la tabla de servicio de mensaje llamando al método [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) . 
  
Las siguientes propiedades que conforman la columna necesaria establecida en la tabla de servicios de mensaje:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** es el nombre que se puede mostrar para el servicio de mensajes y la columna de clave de ordenación predeterminado. 
  
 **PR_INSTANCE_KEY** sirve la columna de índice para la tabla de caracteres que identifica una fila. 
  
 **PR_RESOURCE_FLAGS** describe las capacidades del servicio de mensajes. 
  
 **PR_SERVICE_DLL_NAME** es el nombre del archivo DLL que contiene la implementación del servicio de mensajes. 
  
 **PR_SERVICE_ENTRY_NAME** es el nombre de la función de punto de entrada del servicio de mensajes que se ajusta al prototipo [MSGSERVICEENTRY](msgserviceentry.md) . 
  
 **PR_SERVICE_NAME** es una entrada obligatoria en la sección **[Services]** en MAPISVC.INF. El valor de esta propiedad nunca cambiará o localizado. **PR_SERVICE_NAME** puede utilizarse para identificar mediante programación el servicio de mensajes. 
  
 **PR_SERVICE_SUPPORT_FILES** es una lista de archivos que debe estar instalado con el servicio de mensajes. 
  
 **PR_SERVICE_UID** es un identificador único para el servicio de mensajes. 
  
## <a name="see-also"></a>Recursos adicionales



[Tablas MAPI](mapi-tables.md)

