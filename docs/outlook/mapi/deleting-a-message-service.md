---
title: Eliminación de un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316866"
---
# <a name="deleting-a-message-service"></a>Eliminación de un servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para eliminar un servicio de mensajes de un perfil**
  
1. Llame a **IMAPISession:: GetMsgServiceTable** para obtener acceso a la tabla de servicio de mensajes. 
    
2. Busque la fila del servicio de mensajes y pase su columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) en el parámetro _Lpuid_ a [IMsgServiceAdmin::D eletemsgservice](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** llama a la función de punto de entrada del servicio de mensajes con el parámetro _ULCONTEXT_ establecido en MSG_SERVICE_DELETE. Los servicios de mensajes realizan todas las tareas de limpieza en este momento antes de que se quiten del perfil. 
  

