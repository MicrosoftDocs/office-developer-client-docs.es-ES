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
ms.openlocfilehash: 07305f712fd925b206ce18a32f8f5a24f199ccbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817838"
---
# <a name="iostxinitsync"></a><span data-ttu-id="637fa-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="637fa-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="637fa-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="637fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="637fa-105">Informa que el almacén de mensajes local que sincronización está a punto de inicio.</span><span class="sxs-lookup"><span data-stu-id="637fa-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="637fa-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="637fa-106">Parameters</span></span>

 <span data-ttu-id="637fa-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="637fa-107">_ulFlags_</span></span>
  
> <span data-ttu-id="637fa-108">[entrada] Marcas para determinar el comportamiento adecuado durante la sincronización.</span><span class="sxs-lookup"><span data-stu-id="637fa-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="637fa-109">Outlook utiliza estos marcadores en cada estado de la máquina de estado de replicación para determinar la información que debe suministrar para el cliente.</span><span class="sxs-lookup"><span data-stu-id="637fa-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="637fa-110">Por ejemplo, si el cliente pasa **SYNC_ONLY_ASSOCIATED**, Outlook solo devuelven información relacionada con los elementos asociados (u ocultos).</span><span class="sxs-lookup"><span data-stu-id="637fa-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="637fa-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="637fa-111">See also</span></span>



[<span data-ttu-id="637fa-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="637fa-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="637fa-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="637fa-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="637fa-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="637fa-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="637fa-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="637fa-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="637fa-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="637fa-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="637fa-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="637fa-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="637fa-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="637fa-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="637fa-119">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="637fa-119">MAPI Constants</span></span>](mapi-constants.md)

