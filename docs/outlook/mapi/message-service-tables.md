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
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422498"
---
# <a name="message-service-tables"></a>Tablas de servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La tabla servicio de mensajes contiene información sobre los servicios de mensajes en el perfil actual. Hay una tabla de servicio de mensajes para cada sesión MAPI, implementada por MAPI y utilizada por aplicaciones cliente de uso especial que proporcionan compatibilidad con la configuración. 
  
La tabla de servicio de mensajes es una tabla estática.
  
Los clientes tienen acceso a la tabla de servicio de mensajes llamando al método [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) . 
  
Las siguientes propiedades conforman la columna obligatoria que se establece en la tabla de servicio de mensajes:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** es el nombre que se puede mostrar para el servicio de mensajes y la columna de criterio de ordenación predeterminada. 
  
 **PR_INSTANCE_KEY** sirve como columna de índice de la tabla, identificando de forma única una fila. 
  
 **PR_RESOURCE_FLAGS** describe las capacidades del servicio de mensajes. 
  
 **PR_SERVICE_DLL_NAME** es el nombre de la dll que contiene la implementación del servicio de mensajes. 
  
 **PR_SERVICE_ENTRY_NAME** es el nombre de la función de punto de entrada del servicio de mensajería que se ajusta al prototipo [MSGSERVICEENTRY](msgserviceentry.md) . 
  
 **PR_SERVICE_NAME** es una entrada obligatoria en la sección **[Services]** del archivo MAPISVC. inf. El valor de esta propiedad nunca se cambiará ni se localizará. **PR_SERVICE_NAME** puede usarse para identificar el servicio de mensajes mediante programación. 
  
 **PR_SERVICE_SUPPORT_FILES** es una lista de los archivos que se deben instalar con el servicio de mensajes. 
  
 **PR_SERVICE_UID** es un identificador único para el servicio de mensajes. 
  
## <a name="see-also"></a>Ver también



[Tablas MAPI](mapi-tables.md)

