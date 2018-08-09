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
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816562"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="20cbc-103">Copiar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="20cbc-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="20cbc-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20cbc-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="20cbc-105">**Para copiar un servicio de mensajes a un perfil**</span><span class="sxs-lookup"><span data-stu-id="20cbc-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="20cbc-106">Llame a [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="20cbc-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="20cbc-107">Cuando se copia un servicio de mensajes, la nueva instancia del servicio se configura en exactamente de la misma manera que el original.</span><span class="sxs-lookup"><span data-stu-id="20cbc-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="20cbc-108">En ocasiones, **CopyMsgService** devuelve el error MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="20cbc-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="20cbc-109">La causa más común de este error devuelto es un servicio de mensajes que no permitir que se duplican.</span><span class="sxs-lookup"><span data-stu-id="20cbc-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

