---
title: Eliminar un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 34d9d6d428f39765e739ce856f3666d07b457d52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816654"
---
# <a name="deleting-a-message-service"></a>Eliminar un servicio de mensajes

  
  
**Hace referencia a**: Outlook 
  
 **Para eliminar un servicio de mensajes de un perfil**
  
1. Llame a **IMAPISession::GetMsgServiceTable** para obtener acceso a la tabla de mensajes de servicio. 
    
2. Busque la fila para el servicio de mensajes y pasar su columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) en el parámetro _lpuid_ a [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** llama a la función de punto de entrada del servicio de mensajes con el parámetro _ulContext_ establecido en MSG_SERVICE_DELETE. Servicios de mensajes realizan cualquier tareas de limpieza en este momento antes de que se quitan de los perfiles. 
  

