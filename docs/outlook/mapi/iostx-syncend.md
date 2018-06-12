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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 66542d2cc7600ecbcd8de9043b6b40559744c2ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817849"
---
# <a name="iostxsyncend"></a><span data-ttu-id="b3d56-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="b3d56-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="b3d56-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3d56-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3d56-105">Finaliza la sincronización en el estado actual y sale de ese estado.</span><span class="sxs-lookup"><span data-stu-id="b3d56-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="b3d56-106">Notas</span><span class="sxs-lookup"><span data-stu-id="b3d56-106">Remarks</span></span>

<span data-ttu-id="b3d56-107">El cliente debe llamar a **IOSTX::SyncEnd** para cada llamada a [IOSTX::SyncBeg](iostx-syncbeg.md).</span><span class="sxs-lookup"><span data-stu-id="b3d56-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="b3d56-108">La estructura de datos correspondiente contiene información para indicar si el cliente ha completado correctamente el estado actual para que Outlook puede limpiar su estado interno.</span><span class="sxs-lookup"><span data-stu-id="b3d56-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3d56-109">Ver también</span><span class="sxs-lookup"><span data-stu-id="b3d56-109">See also</span></span>



[<span data-ttu-id="b3d56-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b3d56-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="b3d56-111">IOSTX::Initsync</span><span class="sxs-lookup"><span data-stu-id="b3d56-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="b3d56-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="b3d56-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="b3d56-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="b3d56-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="b3d56-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="b3d56-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="b3d56-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="b3d56-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="b3d56-116">IOSTX: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b3d56-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="b3d56-117">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b3d56-117">MAPI Constants</span></span>](mapi-constants.md)

