---
title: Copiar un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8388d14446a230b032e49ad0d614c85e79b8ece8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573722"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="23b57-103">Copiar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="23b57-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="23b57-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23b57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="23b57-105">**Para copiar un servicio de mensajes a un perfil**</span><span class="sxs-lookup"><span data-stu-id="23b57-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="23b57-106">Llame a [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="23b57-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="23b57-107">Cuando se copia un servicio de mensajes, la nueva instancia del servicio se configura en exactamente de la misma manera que el original.</span><span class="sxs-lookup"><span data-stu-id="23b57-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="23b57-108">En ocasiones, **CopyMsgService** devuelve el error MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="23b57-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="23b57-109">La causa más común de este error devuelto es un servicio de mensajes que no permitir que se duplican.</span><span class="sxs-lookup"><span data-stu-id="23b57-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

