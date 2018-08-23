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
ms.openlocfilehash: 6a8b0f8fc8c296fe4022ac28623b83d270472ca3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590697"
---
# <a name="adding-a-message-service"></a>Agregar un servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para agregar un nuevo servicio de mensajes a un perfil y tener acceso al servicio de mensaje nuevo**
  
Llame a [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx** realiza las tareas siguientes: 
  
1. Copia toda la información relevante para el servicio de mensajes que se encuentra en el archivo MAPISVC. Archivo INF, creación de una sección de perfil para cada sección del proveedor.
    
2. Llamadas de función de punto de entrada del servicio de mensajes, **MSGSERVICEENTRY**, con el parámetro _ulContext_ establecido en MSG_SERVICE_CREATE. 
    
3. Establece y recupera la propiedad de **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) del servicio de mensajes.
    
 **Para tener acceso a cualquier servicio de mensajes recién agregado**
  
1. Llame a [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para recuperar la tabla de mensajes de servicio. 
    
2. Llamar al método [IMAPITable::Advise](imapitable-advise.md) de la tabla de servicio de mensaje para registrar para las notificaciones de tabla. 
    
3. Cuando MAPI envía una notificación de TABLE_ROW_ADDED, busque el identificador de entrada del servicio de mensajes recién agregada en la estructura de [SRow](srow.md) incluida en la estructura [TABLE_NOTIFICATION](table_notification.md) . 
    

