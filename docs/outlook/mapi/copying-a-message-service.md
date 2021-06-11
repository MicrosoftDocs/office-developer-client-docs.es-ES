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
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425396"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="8a3a4-103">Copiar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="8a3a4-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="8a3a4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a3a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8a3a4-105">**Para copiar un servicio de mensajes en un perfil**</span><span class="sxs-lookup"><span data-stu-id="8a3a4-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="8a3a4-106">Llame [a IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="8a3a4-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="8a3a4-107">Cuando se copia un servicio de mensajes, la nueva instancia del servicio se configura exactamente del mismo modo que el original.</span><span class="sxs-lookup"><span data-stu-id="8a3a4-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="8a3a4-108">A **veces, CopyMsgService** devuelve el error MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="8a3a4-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="8a3a4-109">La causa más común de esta devolución de errores es un servicio de mensajes que no se permite duplicarse.</span><span class="sxs-lookup"><span data-stu-id="8a3a4-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

