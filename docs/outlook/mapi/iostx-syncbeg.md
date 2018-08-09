---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ddc61aa42b1087ed5f0ecb7986125ceef27cddce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817839"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="d2608-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="d2608-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="d2608-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2608-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2608-105">Prepara el almacén local para la sincronización en un estado determinado y recupera la información necesaria para replicar.</span><span class="sxs-lookup"><span data-stu-id="d2608-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="d2608-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2608-106">Parameters</span></span>

 <span data-ttu-id="d2608-107">_uiSync_</span><span class="sxs-lookup"><span data-stu-id="d2608-107">_uiSync_</span></span>
  
>  <span data-ttu-id="d2608-108">[entrada] El estado que se especifique el almacén local.</span><span class="sxs-lookup"><span data-stu-id="d2608-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="d2608-109">La siguiente es una lista de identificadores de estado:</span><span class="sxs-lookup"><span data-stu-id="d2608-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="d2608-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="d2608-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="d2608-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="d2608-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="d2608-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="d2608-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="d2608-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="d2608-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="d2608-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="d2608-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="d2608-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="d2608-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="d2608-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="d2608-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="d2608-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="d2608-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="d2608-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="d2608-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="d2608-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="d2608-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="d2608-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="d2608-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="d2608-121">_PPV_</span><span class="sxs-lookup"><span data-stu-id="d2608-121">_ppv_</span></span>
  
>  <span data-ttu-id="d2608-122">[en] / [salida] puntero a la estructura de datos correspondiente al estado para escribir.</span><span class="sxs-lookup"><span data-stu-id="d2608-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="d2608-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="d2608-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="d2608-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="d2608-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="d2608-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="d2608-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="d2608-126">SYNC</span><span class="sxs-lookup"><span data-stu-id="d2608-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="d2608-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="d2608-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="d2608-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="d2608-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="d2608-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="d2608-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="d2608-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="d2608-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="d2608-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="d2608-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="d2608-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="d2608-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="d2608-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="d2608-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="d2608-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="d2608-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="d2608-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="d2608-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="d2608-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="d2608-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="d2608-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="d2608-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="d2608-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2608-138">Remarks</span></span>

<span data-ttu-id="d2608-139">El cliente llama a **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** para establecer el resultado de la sincronización y, a continuación, llama a **[IOSTX::SyncEnd](iostx-syncend.md)** para finalizar ese estado.</span><span class="sxs-lookup"><span data-stu-id="d2608-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="d2608-140">El cliente debe llamar a **[IOSTX::SyncEnd](iostx-syncend.md)** para que cada llamada a **IOSTX::SyncBeg** con el fin de determinar si el estado se ha replicado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d2608-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="d2608-141">Una vez que se ha determinado, Outlook puede empezar a limpiar su estado interno.</span><span class="sxs-lookup"><span data-stu-id="d2608-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="d2608-142">La mayoría de estas estructuras contienen [out] o [in] información, lo que permite a Outlook pasar información para el cliente y el cliente para pasar información a Outlook.</span><span class="sxs-lookup"><span data-stu-id="d2608-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="d2608-143">Cuando el cliente llama a **IOSTX::SyncBeg**, Outlook asigna la estructura de datos para un estado determinado y lo inicializa con información de ese estado.</span><span class="sxs-lookup"><span data-stu-id="d2608-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="d2608-144">Se trata de la información [out].</span><span class="sxs-lookup"><span data-stu-id="d2608-144">This is the [out] information.</span></span> <span data-ttu-id="d2608-145">Mientras está en un estado, el cliente actualiza la estructura de datos correspondiente para ese estado.</span><span class="sxs-lookup"><span data-stu-id="d2608-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="d2608-146">Este es el [de] información.</span><span class="sxs-lookup"><span data-stu-id="d2608-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2608-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2608-147">See also</span></span>



[<span data-ttu-id="d2608-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d2608-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="d2608-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="d2608-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="d2608-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="d2608-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="d2608-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="d2608-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="d2608-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="d2608-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="d2608-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="d2608-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="d2608-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2608-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="d2608-155">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d2608-155">MAPI Constants</span></span>](mapi-constants.md)

