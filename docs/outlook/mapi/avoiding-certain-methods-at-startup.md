---
title: Evitar ciertos métodos al inicio
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580638"
---
# <a name="avoiding-certain-methods-at-startup"></a><span data-ttu-id="761f7-103">Evitar ciertos métodos al inicio</span><span class="sxs-lookup"><span data-stu-id="761f7-103">Avoiding Certain Methods at Startup</span></span>

 
  
<span data-ttu-id="761f7-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="761f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="761f7-105">Para mejorar el rendimiento en tiempo de inicio, evitar llamadas siguientes:</span><span class="sxs-lookup"><span data-stu-id="761f7-105">To improve performance at startup time, avoid making the following calls:</span></span>
  
- [<span data-ttu-id="761f7-106">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="761f7-106">IMAPISession::EnumAdrTypes</span></span>](imapisession-enumadrtypes.md)
    
- [<span data-ttu-id="761f7-107">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="761f7-107">IMAPISession::GetStatusTable</span></span>](imapisession-getstatustable.md)
    
- [<span data-ttu-id="761f7-108">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="761f7-108">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
    
- [<span data-ttu-id="761f7-109">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="761f7-109">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
    
- [<span data-ttu-id="761f7-110">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="761f7-110">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
    
<span data-ttu-id="761f7-111">La llamada a **IMAPIStatus::ValidateState** afecta al rendimiento únicamente cuando se realizan en la cola de MAPI o el subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="761f7-111">The call to **IMAPIStatus::ValidateState** affects performance only when made on either the MAPI spooler or the MAPI subsystem.</span></span> <span data-ttu-id="761f7-112">La razón por la que estos métodos ralentizar el procesamiento de inicio es porque no se completan hasta que la cola MAPI ha finalizado sus tareas de inicio.</span><span class="sxs-lookup"><span data-stu-id="761f7-112">The reason that these methods slow startup processing is because they cannot complete until the MAPI spooler has finished its startup tasks.</span></span> 
  
<span data-ttu-id="761f7-113">También debe evitar buscar en el almacén de mensajes en tiempo de inicio.</span><span class="sxs-lookup"><span data-stu-id="761f7-113">You should also avoid searching the message store at startup time.</span></span> <span data-ttu-id="761f7-114">Realizar la llamada de [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) cuando ha terminado el procesamiento de inicio.</span><span class="sxs-lookup"><span data-stu-id="761f7-114">Make your [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) call when startup processing has finished.</span></span> 
  

