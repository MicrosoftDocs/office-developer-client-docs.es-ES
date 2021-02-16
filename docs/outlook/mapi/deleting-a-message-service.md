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
# <a name="deleting-a-message-service"></a><span data-ttu-id="7ba92-103">Eliminación de un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="7ba92-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="7ba92-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ba92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="7ba92-105">**Para eliminar un servicio de mensajes de un perfil**</span><span class="sxs-lookup"><span data-stu-id="7ba92-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="7ba92-106">Llame **a IMAPISession::GetMsgServiceTable** para obtener acceso a la tabla del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7ba92-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="7ba92-107">Busque la fila para el servicio de mensajes y pase su columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) en el parámetro  _lpuid_ a [IMsgServiceAdmin::D eleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="7ba92-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="7ba92-108">**DeleteMsgService llama** a la función de punto de entrada del servicio de mensajes con el parámetro  _ulContext_ establecido en MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="7ba92-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="7ba92-109">Los servicios de mensajes realizan tareas de limpieza en este momento antes de quitarse del perfil.</span><span class="sxs-lookup"><span data-stu-id="7ba92-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

