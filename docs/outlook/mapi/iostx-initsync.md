---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b9086383b45d40d5839284ac785d72438be60e00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317195"
---
# <a name="iostxinitsync"></a><span data-ttu-id="81b9f-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="81b9f-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="81b9f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81b9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81b9f-105">Informa al almacén de mensajes local que la sincronización está a punto de iniciarse.</span><span class="sxs-lookup"><span data-stu-id="81b9f-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="81b9f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="81b9f-106">Parameters</span></span>

 <span data-ttu-id="81b9f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81b9f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="81b9f-108">a Marcas para determinar el comportamiento adecuado durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="81b9f-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="81b9f-109">Outlook usa estas marcas en cada estado de la máquina de estado de replicación para determinar la información que debe proporcionar para el cliente.</span><span class="sxs-lookup"><span data-stu-id="81b9f-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="81b9f-110">Por ejemplo, si el cliente pasa **SYNC_ONLY_ASSOCIATED**, Outlook solo devolverá información relacionada con los elementos asociados (u ocultos).</span><span class="sxs-lookup"><span data-stu-id="81b9f-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="81b9f-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="81b9f-111">See also</span></span>



[<span data-ttu-id="81b9f-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="81b9f-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="81b9f-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="81b9f-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="81b9f-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="81b9f-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="81b9f-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="81b9f-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="81b9f-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="81b9f-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="81b9f-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="81b9f-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="81b9f-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81b9f-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="81b9f-119">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="81b9f-119">MAPI Constants</span></span>](mapi-constants.md)

