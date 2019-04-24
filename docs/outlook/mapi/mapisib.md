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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270213"
---
# <a name="mapisib"></a><span data-ttu-id="33f56-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="33f56-103">MAPISIB</span></span>

  
  
<span data-ttu-id="33f56-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33f56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33f56-105">Esta estructura se usa con [IMAPISync:: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="33f56-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="33f56-106">Members</span><span class="sxs-lookup"><span data-stu-id="33f56-106">Members</span></span>

 <span data-ttu-id="33f56-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="33f56-107">**ulSize**</span></span>
  
> <span data-ttu-id="33f56-108">El tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="33f56-108">The size of the structure.</span></span>
    
 <span data-ttu-id="33f56-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="33f56-109">**ulFlags**</span></span>
  
> <span data-ttu-id="33f56-110">Marca que indica el tipo de sincronización. Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="33f56-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="33f56-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="33f56-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="33f56-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="33f56-112">0x00000200</span></span>  <br/> |<span data-ttu-id="33f56-113">Enviar el mensaje al servidor (no actualmente en uso).</span><span class="sxs-lookup"><span data-stu-id="33f56-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="33f56-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="33f56-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="33f56-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="33f56-115">0x00000001</span></span>  <br/> |<span data-ttu-id="33f56-116">Inserta los cambios en la jerarquía del servidor.</span><span class="sxs-lookup"><span data-stu-id="33f56-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="33f56-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="33f56-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="33f56-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="33f56-118">0x00000002</span></span>  <br/> |<span data-ttu-id="33f56-119">Extraer los cambios en la jerarquía del servidor.</span><span class="sxs-lookup"><span data-stu-id="33f56-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="33f56-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="33f56-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="33f56-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="33f56-121">0x00000040</span></span>  <br/> |<span data-ttu-id="33f56-122">Insertar los cambios de mensajes en el servidor.</span><span class="sxs-lookup"><span data-stu-id="33f56-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="33f56-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="33f56-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="33f56-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="33f56-124">0x00000080</span></span>  <br/> |<span data-ttu-id="33f56-125">Extraer los cambios de mensajes del servidor.</span><span class="sxs-lookup"><span data-stu-id="33f56-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="33f56-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="33f56-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="33f56-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="33f56-127">0x20000000</span></span>  <br/> |<span data-ttu-id="33f56-128">La sincronización ha sido iniciada por el usuario y debe tener una prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="33f56-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="33f56-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="33f56-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="33f56-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="33f56-130">0x02000000</span></span>  <br/> |<span data-ttu-id="33f56-131">Solo debe sincronizar los encabezados y no los cuerpos completos.</span><span class="sxs-lookup"><span data-stu-id="33f56-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="33f56-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="33f56-132">**psesSync**</span></span>
  
> <span data-ttu-id="33f56-133">A Un puntero a la sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="33f56-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="33f56-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="33f56-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="33f56-135">A Puntero a la interfaz en la que se va a proporcionar el progreso.</span><span class="sxs-lookup"><span data-stu-id="33f56-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="33f56-136">Se puede usar para consultar la interfaz de [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="33f56-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="33f56-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="33f56-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="33f56-138">CONTEMPLA Evento que se producirá cuando se complete el subproceso que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="33f56-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="33f56-139">El puntero debe ser válido porque contendrá el evento.</span><span class="sxs-lookup"><span data-stu-id="33f56-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33f56-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="33f56-140">See also</span></span>



[<span data-ttu-id="33f56-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33f56-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="33f56-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33f56-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

