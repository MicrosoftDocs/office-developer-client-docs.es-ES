---
title: Agregar un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407238"
---
# <a name="adding-a-message-service"></a>Agregar un servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para agregar un nuevo servicio de mensajes a un perfil y obtener acceso al nuevo servicio de mensajes**
  
Llame [a IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx** realiza las siguientes tareas: 
  
1. Copia toda la información relevante para el servicio de mensajes que se encuentra en MAPISVC. INF, creando una sección de perfil para cada sección de proveedor.
    
2. Llama a la función de punto de entrada del servicio de mensajes, **MSGSERVICEENTRY**, con el parámetro  _ulContext_ establecido en MSG_SERVICE_CREATE. 
    
3. Establece y recupera la propiedad del servicio de **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)).
    
 **Para obtener acceso a cualquier servicio de mensajes recién agregado**
  
1. Llame [a IMsgServiceAdmin::GetMsgServiceTable para](imsgserviceadmin-getmsgservicetable.md) recuperar la tabla de servicio de mensajes. 
    
2. Llama al método [IMAPITable::Advise](imapitable-advise.md) de la tabla de servicio de mensajes para registrar las notificaciones de tabla. 
    
3. Cuando MAPI envía una notificación TABLE_ROW_ADDED, busque el identificador de entrada del servicio de mensajes recién agregado en la estructura [SRow](srow.md) incluida en la [TABLE_NOTIFICATION.](table_notification.md) 
    

