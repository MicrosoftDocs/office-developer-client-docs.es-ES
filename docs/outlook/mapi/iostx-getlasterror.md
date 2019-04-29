---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9c29011ae2e9b59a7a0a38148fa6c5b673fd9590
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422302"
---
# <a name="iostxgetlasterror"></a><span data-ttu-id="9abc4-103">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9abc4-103">IOSTX::GetLastError</span></span>

  
  
<span data-ttu-id="9abc4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9abc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9abc4-105">Obtiene información extendida sobre el último error.</span><span class="sxs-lookup"><span data-stu-id="9abc4-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="9abc4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9abc4-106">Parameters</span></span>

 <span data-ttu-id="9abc4-107">_Valores_</span><span class="sxs-lookup"><span data-stu-id="9abc4-107">_hResult_</span></span>
  
>  <span data-ttu-id="9abc4-108">a Código de error.</span><span class="sxs-lookup"><span data-stu-id="9abc4-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="9abc4-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9abc4-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="9abc4-110">[entrada] Marcadores para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="9abc4-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="9abc4-111">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="9abc4-111">This must be 0.</span></span> 
    
 <span data-ttu-id="9abc4-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="9abc4-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="9abc4-113">contempla Puntero a la estructura **MAPIERROR** que contiene la información extendida del error.</span><span class="sxs-lookup"><span data-stu-id="9abc4-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="9abc4-114">Consulte mapidefs. h para obtener la definición de tipo de **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="9abc4-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9abc4-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="9abc4-115">See also</span></span>



[<span data-ttu-id="9abc4-116">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="9abc4-116">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="9abc4-117">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="9abc4-117">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="9abc4-118">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="9abc4-118">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="9abc4-119">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="9abc4-119">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="9abc4-120">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="9abc4-120">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="9abc4-121">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="9abc4-121">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="9abc4-122">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9abc4-122">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="9abc4-123">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9abc4-123">MAPI Constants</span></span>](mapi-constants.md)

