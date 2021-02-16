---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418711"
---
# <a name="mapisib"></a><span data-ttu-id="ad7f9-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="ad7f9-103">MAPISIB</span></span>

  
  
<span data-ttu-id="ad7f9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad7f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad7f9-105">Esta estructura se usa con [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="ad7f9-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a><span data-ttu-id="ad7f9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ad7f9-106">Members</span></span>

 <span data-ttu-id="ad7f9-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="ad7f9-107">**ulSize**</span></span>
  
> <span data-ttu-id="ad7f9-108">Tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="ad7f9-108">The size of the structure.</span></span>
    
 <span data-ttu-id="ad7f9-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="ad7f9-109">**ulFlags**</span></span>
  
> <span data-ttu-id="ad7f9-110">Marca que indica el tipo de sincronización. Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="ad7f9-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="ad7f9-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="ad7f9-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="ad7f9-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="ad7f9-112">0x00000200</span></span>  <br/> |<span data-ttu-id="ad7f9-113">Envíe el mensaje al servidor (no está en uso actualmente).</span><span class="sxs-lookup"><span data-stu-id="ad7f9-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="ad7f9-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="ad7f9-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="ad7f9-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ad7f9-115">0x00000001</span></span>  <br/> |<span data-ttu-id="ad7f9-116">Cambios de jerarquía de inserción en el servidor.</span><span class="sxs-lookup"><span data-stu-id="ad7f9-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="ad7f9-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="ad7f9-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="ad7f9-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ad7f9-118">0x00000002</span></span>  <br/> |<span data-ttu-id="ad7f9-119">Extraer cambios de jerarquía del servidor.</span><span class="sxs-lookup"><span data-stu-id="ad7f9-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="ad7f9-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="ad7f9-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="ad7f9-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="ad7f9-121">0x00000040</span></span>  <br/> |<span data-ttu-id="ad7f9-122">Cambios de mensajes de inserción en el servidor.</span><span class="sxs-lookup"><span data-stu-id="ad7f9-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="ad7f9-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="ad7f9-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="ad7f9-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="ad7f9-124">0x00000080</span></span>  <br/> |<span data-ttu-id="ad7f9-125">Extraer cambios de mensajes del servidor.</span><span class="sxs-lookup"><span data-stu-id="ad7f9-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="ad7f9-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="ad7f9-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="ad7f9-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="ad7f9-127">0x20000000</span></span>  <br/> |<span data-ttu-id="ad7f9-128">El usuario inició la sincronización y debe ser de mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="ad7f9-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="ad7f9-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="ad7f9-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="ad7f9-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="ad7f9-130">0x02000000</span></span>  <br/> |<span data-ttu-id="ad7f9-131">Solo deben sincronizarse los encabezados y no los cuerpos completos.</span><span class="sxs-lookup"><span data-stu-id="ad7f9-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="ad7f9-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="ad7f9-132">**psesSync**</span></span>
  
> <span data-ttu-id="ad7f9-133">[ENTRADA] Puntero a la sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad7f9-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="ad7f9-134">**golcallBack**</span><span class="sxs-lookup"><span data-stu-id="ad7f9-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="ad7f9-135">[ENTRADA] Puntero a la interfaz en la que se va a proporcionar el progreso.</span><span class="sxs-lookup"><span data-stu-id="ad7f9-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="ad7f9-136">Se puede usar para consultar la interfaz de [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="ad7f9-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="ad7f9-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="ad7f9-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="ad7f9-138">[SALIDA] Evento que se producirá cuando se complete el subproceso que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="ad7f9-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="ad7f9-139">El puntero debe ser válido porque contendrá el evento.</span><span class="sxs-lookup"><span data-stu-id="ad7f9-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad7f9-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ad7f9-140">See also</span></span>



[<span data-ttu-id="ad7f9-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad7f9-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="ad7f9-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad7f9-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

