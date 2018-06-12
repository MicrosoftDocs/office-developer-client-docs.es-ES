---
title: Adición de un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: a7735be5cfb8ff0716b6bd6eba4951563bb938ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816380"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="ada5d-103">Adición de un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="ada5d-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="ada5d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ada5d-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="ada5d-105">**Para agregar un nuevo servicio de mensajes a un perfil y tener acceso al servicio de mensaje nuevo**</span><span class="sxs-lookup"><span data-stu-id="ada5d-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="ada5d-106">Llame a [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="ada5d-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="ada5d-107">**CreateMsgServiceEx** realiza las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="ada5d-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="ada5d-108">Copia toda la información relevante para el servicio de mensajes que se encuentra en el archivo MAPISVC. Archivo INF, creación de una sección de perfil para cada sección del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ada5d-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="ada5d-109">Llamadas de función de punto de entrada del servicio de mensajes, **MSGSERVICEENTRY**, con el parámetro _ulContext_ establecido en MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="ada5d-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="ada5d-110">Establece y recupera la propiedad de **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ada5d-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="ada5d-111">**Para tener acceso a cualquier servicio de mensajes recién agregado**</span><span class="sxs-lookup"><span data-stu-id="ada5d-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="ada5d-112">Llame a [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para recuperar la tabla de mensajes de servicio.</span><span class="sxs-lookup"><span data-stu-id="ada5d-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="ada5d-113">Llamar al método [IMAPITable::Advise](imapitable-advise.md) de la tabla de servicio de mensaje para registrar para las notificaciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="ada5d-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="ada5d-114">Cuando MAPI envía una notificación de TABLE_ROW_ADDED, busque el identificador de entrada del servicio de mensajes recién agregada en la estructura de [SRow](srow.md) incluida en la estructura [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="ada5d-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

