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
ms.openlocfilehash: 74a4e299da6c0637c3da70c329569266d43dbd9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817840"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="40c85-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="40c85-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="40c85-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40c85-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40c85-105">Establece el resultado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="40c85-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="40c85-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40c85-106">Parameters</span></span>

 <span data-ttu-id="40c85-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="40c85-107">_hrSync_</span></span>
  
>  <span data-ttu-id="40c85-108">[entrada] El resultado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="40c85-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="40c85-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40c85-109">Remarks</span></span>

<span data-ttu-id="40c85-110">Llame a **IOSTX::SetSyncResult** antes de llamar a **IOSTX::SyncEnd** para informar el almacén local del resultado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="40c85-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40c85-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="40c85-111">See also</span></span>



[<span data-ttu-id="40c85-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="40c85-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="40c85-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="40c85-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="40c85-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="40c85-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="40c85-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="40c85-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="40c85-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="40c85-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="40c85-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="40c85-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="40c85-118">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="40c85-118">MAPI Constants</span></span>](mapi-constants.md)

