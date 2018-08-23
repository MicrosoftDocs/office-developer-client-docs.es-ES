---
title: IOSTX IUnknown
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
ms.openlocfilehash: 9c9252e83ce212bacf185d0eedb75d30617f9807
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581751"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="b1c95-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1c95-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="b1c95-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1c95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1c95-105">Proporciona métodos de sincronización.</span><span class="sxs-lookup"><span data-stu-id="b1c95-105">Provides synchronization methods.</span></span> <span data-ttu-id="b1c95-106">Esta interfaz recupera la información necesaria para replicar los cambios locales en el servidor y los cambios del servidor en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="b1c95-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1c95-107">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="b1c95-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="b1c95-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="b1c95-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="b1c95-109">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="b1c95-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b1c95-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="b1c95-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b1c95-111">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="b1c95-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b1c95-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b1c95-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="b1c95-113">Obtiene información sobre el último error ampliada.</span><span class="sxs-lookup"><span data-stu-id="b1c95-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="b1c95-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="b1c95-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="b1c95-115">Informa el almacén local que sincronización está a punto de inicio.</span><span class="sxs-lookup"><span data-stu-id="b1c95-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="b1c95-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="b1c95-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="b1c95-117">Prepara el almacén local para la sincronización en un estado determinado y recupera la información necesaria para replicar.</span><span class="sxs-lookup"><span data-stu-id="b1c95-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="b1c95-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="b1c95-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="b1c95-119">Finaliza la sincronización en el estado actual y sale de ese estado.</span><span class="sxs-lookup"><span data-stu-id="b1c95-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="b1c95-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="b1c95-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="b1c95-121">Inicia la sincronización para un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b1c95-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="b1c95-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="b1c95-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="b1c95-123">Finaliza la sincronización para un encabezado de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b1c95-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="b1c95-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="b1c95-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="b1c95-125">Establece el resultado de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="b1c95-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="b1c95-126">*Miembro de marcador de posición*</span><span class="sxs-lookup"><span data-stu-id="b1c95-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="b1c95-127">*No se admiten o documentado.*</span><span class="sxs-lookup"><span data-stu-id="b1c95-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1c95-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1c95-128">Remarks</span></span>

<span data-ttu-id="b1c95-129">Cuando un cliente de carga o sincroniza las carpetas y el contenido de la carpeta en un almacén local, mueve el almacén local de un estado a otro como se muestra en el diagrama de transición de estado en [Acerca de la máquina de estado de replicación](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="b1c95-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="b1c95-130">El siguiente es el orden de eventos para el cliente mover el almacén local de un estado a otro:</span><span class="sxs-lookup"><span data-stu-id="b1c95-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="b1c95-131">El cliente llama a **IOSTX::InitSync** para informarle de que la replicación esté a punto de iniciar el almacén local.</span><span class="sxs-lookup"><span data-stu-id="b1c95-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="b1c95-132">Dependiendo de la dirección de la replicación y la replicación de objetos, el cliente llama a **IOSTX::SyncBeg** para comenzar la replicación en el estado apropiado.</span><span class="sxs-lookup"><span data-stu-id="b1c95-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="b1c95-133">Outlook proporciona al cliente la información necesaria y el cliente realiza la replicación.</span><span class="sxs-lookup"><span data-stu-id="b1c95-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="b1c95-134">El cliente llama a **IOSTX::SetSyncResult** para devolver el resultado de la replicación.</span><span class="sxs-lookup"><span data-stu-id="b1c95-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="b1c95-135">El cliente llama a **IOSTX::SyncEnd** para finalizar la replicación, proporcionar la información necesaria para la replicación posterior de Outlook.</span><span class="sxs-lookup"><span data-stu-id="b1c95-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="b1c95-136">En particular, cuando la descarga de elementos de mensaje, el cliente utiliza **IOSTX::SyncHdrBeg** y **IOSTX::SyncHdrEnd** para actualizar un elemento de mensaje completo con el encabezado del mensaje en el almacén local:</span><span class="sxs-lookup"><span data-stu-id="b1c95-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="b1c95-137">Una vez **IOSTX::SyncHdrBeg**, local almacenar transiciones en el estado del encabezado de mensaje de descarga.</span><span class="sxs-lookup"><span data-stu-id="b1c95-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="b1c95-138">Outlook proporciona inicialmente el cliente con el encabezado del mensaje actual en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="b1c95-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="b1c95-139">El cliente descarga un elemento de mensaje completo junto con el encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b1c95-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="b1c95-140">Outlook actualiza el elemento en el almacén local con el elemento de mensaje completo.</span><span class="sxs-lookup"><span data-stu-id="b1c95-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1c95-141">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b1c95-141">See also</span></span>



[<span data-ttu-id="b1c95-142">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="b1c95-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b1c95-143">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b1c95-143">MAPI Constants</span></span>](mapi-constants.md)

