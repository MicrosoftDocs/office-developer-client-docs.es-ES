---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 78ccf72f17ec350d77f2d22d0e6d2fa7c3d97543
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332147"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="42589-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="42589-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="42589-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42589-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42589-105">Establece el resultado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="42589-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="42589-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="42589-106">Parameters</span></span>

 <span data-ttu-id="42589-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="42589-107">_hrSync_</span></span>
  
>  <span data-ttu-id="42589-108">a Resultado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="42589-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="42589-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42589-109">Remarks</span></span>

<span data-ttu-id="42589-110">Llame a **IOSTX:: SetSyncResult** antes de llamar a **IOSTX:: SyncEnd** para informar al almacén local del resultado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="42589-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42589-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="42589-111">See also</span></span>



[<span data-ttu-id="42589-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="42589-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="42589-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="42589-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="42589-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="42589-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="42589-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="42589-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="42589-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="42589-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="42589-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="42589-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="42589-118">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="42589-118">MAPI Constants</span></span>](mapi-constants.md)

