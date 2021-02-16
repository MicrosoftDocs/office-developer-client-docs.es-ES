---
title: Adición de un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407238"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="bfa22-103">Adición de un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="bfa22-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="bfa22-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfa22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="bfa22-105">**Para agregar un nuevo servicio de mensajes a un perfil y obtener acceso al nuevo servicio de mensajes**</span><span class="sxs-lookup"><span data-stu-id="bfa22-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="bfa22-106">Llame [a IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="bfa22-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="bfa22-107">**CreateMsgServiceEx** realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="bfa22-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="bfa22-108">Copia toda la información relevante para el servicio de mensajes que se encuentra en MAPISVC. Archivo INF, creando una sección de perfil para cada sección de proveedor.</span><span class="sxs-lookup"><span data-stu-id="bfa22-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="bfa22-109">Llama a la función de punto de entrada del servicio de mensajes, **MSGSERVICEENTRY**, con el parámetro  _ulContext_ establecido en MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="bfa22-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="bfa22-110">Establece y recupera la propiedad PR_SERVICE_UID **del** servicio de mensajes ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bfa22-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="bfa22-111">**Para obtener acceso a cualquier servicio de mensajes recién agregado**</span><span class="sxs-lookup"><span data-stu-id="bfa22-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="bfa22-112">Llame [a IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para recuperar la tabla del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bfa22-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="bfa22-113">Llame al método [IMAPITable::Advise](imapitable-advise.md) de la tabla de servicio de mensajes para registrarse para recibir notificaciones de tabla.</span><span class="sxs-lookup"><span data-stu-id="bfa22-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="bfa22-114">Cuando MAPI envía una TABLE_ROW_ADDED, busque el identificador de entrada del servicio de mensajes recién agregado en la estructura [SRow](srow.md) incluida en la [estructura TABLE_NOTIFICATION](table_notification.md) búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bfa22-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

