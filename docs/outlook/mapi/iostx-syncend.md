---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fd5b2ed23eba30cbe861a20c4fd100cb8ea1aeb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568843"
---
# <a name="iostxsyncend"></a><span data-ttu-id="f918c-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="f918c-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="f918c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f918c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f918c-105">Finaliza la sincronización en el estado actual y sale de ese estado.</span><span class="sxs-lookup"><span data-stu-id="f918c-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="f918c-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f918c-106">Remarks</span></span>

<span data-ttu-id="f918c-107">El cliente debe llamar a **IOSTX::SyncEnd** para cada llamada a [IOSTX::SyncBeg](iostx-syncbeg.md).</span><span class="sxs-lookup"><span data-stu-id="f918c-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="f918c-108">La estructura de datos correspondiente contiene información para indicar si el cliente ha completado correctamente el estado actual para que Outlook puede limpiar su estado interno.</span><span class="sxs-lookup"><span data-stu-id="f918c-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f918c-109">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f918c-109">See also</span></span>



[<span data-ttu-id="f918c-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f918c-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="f918c-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="f918c-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="f918c-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="f918c-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="f918c-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="f918c-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="f918c-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="f918c-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="f918c-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="f918c-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="f918c-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f918c-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="f918c-117">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f918c-117">MAPI Constants</span></span>](mapi-constants.md)

