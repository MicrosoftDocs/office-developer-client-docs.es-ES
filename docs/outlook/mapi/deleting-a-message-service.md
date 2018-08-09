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
# <a name="deleting-a-message-service"></a><span data-ttu-id="3ebd7-103">Eliminar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="3ebd7-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="3ebd7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ebd7-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="3ebd7-105">**Para eliminar un servicio de mensajes de un perfil**</span><span class="sxs-lookup"><span data-stu-id="3ebd7-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="3ebd7-106">Llame a **IMAPISession::GetMsgServiceTable** para obtener acceso a la tabla de mensajes de servicio.</span><span class="sxs-lookup"><span data-stu-id="3ebd7-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="3ebd7-107">Busque la fila para el servicio de mensajes y pasar su columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) en el parámetro _lpuid_ a [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="3ebd7-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="3ebd7-108">**DeleteMsgService** llama a la función de punto de entrada del servicio de mensajes con el parámetro _ulContext_ establecido en MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="3ebd7-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="3ebd7-109">Servicios de mensajes realizan cualquier tareas de limpieza en este momento antes de que se quitan de los perfiles.</span><span class="sxs-lookup"><span data-stu-id="3ebd7-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

