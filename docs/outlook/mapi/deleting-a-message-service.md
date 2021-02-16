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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428126"
---
# <a name="deleting-a-message-service"></a>Eliminación de un servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para eliminar un servicio de mensajes de un perfil**
  
1. Llame **a IMAPISession::GetMsgServiceTable** para obtener acceso a la tabla del servicio de mensajes. 
    
2. Busque la fila para el servicio de mensajes y pase su columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) en el parámetro  _lpuid_ a [IMsgServiceAdmin::D eleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService llama** a la función de punto de entrada del servicio de mensajes con el parámetro  _ulContext_ establecido en MSG_SERVICE_DELETE. Los servicios de mensajes realizan tareas de limpieza en este momento antes de quitarse del perfil. 
  

