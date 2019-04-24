---
title: Adición de un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328190"
---
# <a name="adding-a-message-service"></a>Adición de un servicio de mensajes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
 **Para agregar un nuevo servicio de mensajes a un perfil y tener acceso al nuevo servicio de mensajes**
  
Llamar a [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx** realiza las siguientes tareas: 
  
1. Copia toda la información relevante para el servicio de mensajes que se encuentra en el MAPISVC. INF, crear una sección de perfil para cada sección de proveedor.
    
2. Llama a la función de punto de entrada del servicio de mensajes, **MSGSERVICEENTRY**, con el parámetro _ULCONTEXT_ establecido en MSG_SERVICE_CREATE. 
    
3. Establece y recupera la propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) del servicio de mensajes.
    
 **Para tener acceso a cualquier servicio de mensajes recién agregado**
  
1. Llame a [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para recuperar la tabla de servicio de mensajes. 
    
2. Llame al método [IMAPITable:: Advise](imapitable-advise.md) de la tabla del servicio de mensajes para registrarse en las notificaciones de tabla. 
    
3. Cuando MAPI envía una notificación TABLE_ROW_ADDED, busque el identificador de entrada del servicio de mensajes recién agregado en la estructura [SRow](srow.md) incluida en la estructura [TABLE_NOTIFICATION](table_notification.md) . 
    

