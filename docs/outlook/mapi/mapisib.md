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
ms.openlocfilehash: a8044eb6647e6f437c87bb4d8b021c62ea15f606
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818278"
---
# <a name="mapisib"></a><span data-ttu-id="5bf1c-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="5bf1c-103">MAPISIB</span></span>

  
  
<span data-ttu-id="5bf1c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bf1c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bf1c-105">Esta estructura se utiliza con [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="5bf1c-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="5bf1c-106">Members</span><span class="sxs-lookup"><span data-stu-id="5bf1c-106">Members</span></span>

 <span data-ttu-id="5bf1c-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="5bf1c-107">**ulSize**</span></span>
  
> <span data-ttu-id="5bf1c-108">El tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5bf1c-108">The size of the structure.</span></span>
    
 <span data-ttu-id="5bf1c-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="5bf1c-109">**ulFlags**</span></span>
  
> <span data-ttu-id="5bf1c-110">Marca que indica el tipo de sincronización. Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5bf1c-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="5bf1c-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="5bf1c-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="5bf1c-112">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="5bf1c-112">0x00000200</span></span>  <br/> |<span data-ttu-id="5bf1c-113">Enviar el mensaje al servidor (que no están en uso).</span><span class="sxs-lookup"><span data-stu-id="5bf1c-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="5bf1c-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="5bf1c-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="5bf1c-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5bf1c-115">0x00000001</span></span>  <br/> |<span data-ttu-id="5bf1c-116">Publicar los cambios de jerarquía en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5bf1c-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="5bf1c-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="5bf1c-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="5bf1c-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5bf1c-118">0x00000002</span></span>  <br/> |<span data-ttu-id="5bf1c-119">Extraer los cambios en la jerarquía del servidor.</span><span class="sxs-lookup"><span data-stu-id="5bf1c-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="5bf1c-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="5bf1c-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="5bf1c-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="5bf1c-121">0x00000040</span></span>  <br/> |<span data-ttu-id="5bf1c-122">Cambios en el mensaje de inserción al servidor.</span><span class="sxs-lookup"><span data-stu-id="5bf1c-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="5bf1c-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="5bf1c-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="5bf1c-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="5bf1c-124">0x00000080</span></span>  <br/> |<span data-ttu-id="5bf1c-125">Extraer los cambios de los mensajes del servidor.</span><span class="sxs-lookup"><span data-stu-id="5bf1c-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="5bf1c-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="5bf1c-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="5bf1c-127">0 x 20000000</span><span class="sxs-lookup"><span data-stu-id="5bf1c-127">0x20000000</span></span>  <br/> |<span data-ttu-id="5bf1c-128">La sincronización iniciada por el usuario y debe ser una prioridad superior.</span><span class="sxs-lookup"><span data-stu-id="5bf1c-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="5bf1c-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="5bf1c-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="5bf1c-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="5bf1c-130">0x02000000</span></span>  <br/> |<span data-ttu-id="5bf1c-131">Sólo se debe sincronizar los encabezados y cuerpos no completas.</span><span class="sxs-lookup"><span data-stu-id="5bf1c-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="5bf1c-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="5bf1c-132">**psesSync**</span></span>
  
> <span data-ttu-id="5bf1c-133">[IN] Un puntero a la sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="5bf1c-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="5bf1c-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="5bf1c-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="5bf1c-135">[IN] Un puntero a la interfaz en la que se va a proporcionar el progreso.</span><span class="sxs-lookup"><span data-stu-id="5bf1c-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="5bf1c-136">Se puede utilizar para consultar la interfaz para [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="5bf1c-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="5bf1c-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="5bf1c-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="5bf1c-138">[OUT] El evento que se producirá cuando se haya completado el subproceso que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="5bf1c-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="5bf1c-139">El puntero debe ser válido debido a que contendrá el evento.</span><span class="sxs-lookup"><span data-stu-id="5bf1c-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bf1c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bf1c-140">See also</span></span>



[<span data-ttu-id="5bf1c-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bf1c-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="5bf1c-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bf1c-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

