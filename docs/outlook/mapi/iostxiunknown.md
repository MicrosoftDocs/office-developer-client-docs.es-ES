---
title: IUnknown IOSTX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6d7de4d6c14179ddaba4e2ad907f1acc1c53b125
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431998"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="6a3ba-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a3ba-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="6a3ba-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a3ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a3ba-105">Proporciona métodos de sincronización.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-105">Provides synchronization methods.</span></span> <span data-ttu-id="6a3ba-106">Esta interfaz recupera la información necesaria para replicar los cambios locales en el servidor y los cambios del servidor en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a3ba-107">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="6a3ba-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="6a3ba-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="6a3ba-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="6a3ba-109">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="6a3ba-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6a3ba-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="6a3ba-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6a3ba-111">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="6a3ba-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6a3ba-112">Volvió</span><span class="sxs-lookup"><span data-stu-id="6a3ba-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="6a3ba-113">Obtiene información extendida sobre el último error.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="6a3ba-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="6a3ba-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="6a3ba-115">Informa al almacén local de que la sincronización está a punto de iniciarse.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="6a3ba-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="6a3ba-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="6a3ba-117">Prepara el almacén local para la sincronización en un estado concreto y recupera la información necesaria para replicar.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="6a3ba-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="6a3ba-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="6a3ba-119">Finaliza la sincronización en el estado actual y sale de ese estado.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="6a3ba-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="6a3ba-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="6a3ba-121">Inicia la sincronización de un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="6a3ba-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="6a3ba-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="6a3ba-123">Termina la sincronización de un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="6a3ba-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="6a3ba-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="6a3ba-125">Establece el resultado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="6a3ba-126">*Marcador de posición de miembro*</span><span class="sxs-lookup"><span data-stu-id="6a3ba-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="6a3ba-127">*No es compatible o documentado.*</span><span class="sxs-lookup"><span data-stu-id="6a3ba-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a3ba-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a3ba-128">Remarks</span></span>

<span data-ttu-id="6a3ba-129">Cuando un cliente carga o sincroniza el contenido de carpetas y carpetas en un almacén local, mueve el almacén local de un estado a otro, tal como se muestra en el diagrama de transición de estado, en [acerca de la máquina de estado de replicación](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="6a3ba-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="6a3ba-130">El siguiente es el orden de los eventos para que el cliente mueva el almacén local de un estado a otro:</span><span class="sxs-lookup"><span data-stu-id="6a3ba-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="6a3ba-131">El cliente llama a **IOSTX:: InitSync** para informar al almacén local de que la replicación está a punto de iniciarse.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="6a3ba-132">En función de la dirección de la replicación y de los objetos que se van a replicar, el cliente llama a **IOSTX:: SyncBeg** para comenzar la replicación en el estado adecuado.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="6a3ba-133">Outlook proporciona al cliente la información necesaria y el cliente realiza la replicación.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="6a3ba-134">El cliente llama a **IOSTX:: SetSyncResult** para devolver el resultado de la replicación.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="6a3ba-135">El cliente llama a **IOSTX:: SyncEnd** para finalizar la replicación, lo que proporciona a Outlook la información necesaria para la replicación subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="6a3ba-136">En concreto, cuando se descargan elementos de mensaje, el cliente usa **IOSTX:: SyncHdrBeg** y **IOSTX:: SyncHdrEnd** para actualizar un elemento de mensaje completo con el encabezado del mensaje en el almacén local:</span><span class="sxs-lookup"><span data-stu-id="6a3ba-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="6a3ba-137">En **IOSTX:: SyncHdrBeg**, el almacén local cambia al estado del encabezado del mensaje de descarga.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="6a3ba-138">Outlook inicialmente proporciona al cliente el encabezado del mensaje actual en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="6a3ba-139">El cliente descarga un elemento de mensaje completo junto con el encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="6a3ba-140">Outlook actualiza el elemento en el almacén local con el elemento de mensaje completo.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a3ba-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="6a3ba-141">See also</span></span>



[<span data-ttu-id="6a3ba-142">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="6a3ba-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="6a3ba-143">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="6a3ba-143">MAPI Constants</span></span>](mapi-constants.md)

