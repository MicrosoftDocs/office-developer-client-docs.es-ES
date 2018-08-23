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
ms.openlocfilehash: f39f721d434f4e54cbfa5d25a3ba626858f2b13e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583571"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="2c51e-103">Eliminar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="2c51e-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="2c51e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c51e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2c51e-105">**Para eliminar un servicio de mensajes de un perfil**</span><span class="sxs-lookup"><span data-stu-id="2c51e-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="2c51e-106">Llame a **IMAPISession::GetMsgServiceTable** para obtener acceso a la tabla de mensajes de servicio.</span><span class="sxs-lookup"><span data-stu-id="2c51e-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="2c51e-107">Busque la fila para el servicio de mensajes y pasar su columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) en el parámetro _lpuid_ a [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="2c51e-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="2c51e-108">**DeleteMsgService** llama a la función de punto de entrada del servicio de mensajes con el parámetro _ulContext_ establecido en MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="2c51e-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="2c51e-109">Servicios de mensajes realizan cualquier tareas de limpieza en este momento antes de que se quitan de los perfiles.</span><span class="sxs-lookup"><span data-stu-id="2c51e-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

