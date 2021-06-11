---
title: Descargar estado de encabezado de mensaje
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417122"
---
# <a name="download-message-header-state"></a><span data-ttu-id="bf0ba-103">Descargar estado de encabezado de mensaje</span><span class="sxs-lookup"><span data-stu-id="bf0ba-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="bf0ba-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf0ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="bf0ba-105">En este tema se describe lo que sucede durante el estado del encabezado del mensaje de descarga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="bf0ba-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bf0ba-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="bf0ba-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf0ba-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="bf0ba-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="bf0ba-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="bf0ba-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="bf0ba-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="bf0ba-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="bf0ba-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="bf0ba-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="bf0ba-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="bf0ba-111">From this state:</span></span>  <br/> |[<span data-ttu-id="bf0ba-112">Estado inactivo</span><span class="sxs-lookup"><span data-stu-id="bf0ba-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="bf0ba-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="bf0ba-113">To this state:</span></span>  <br/> |<span data-ttu-id="bf0ba-114">Estado inactivo</span><span class="sxs-lookup"><span data-stu-id="bf0ba-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="bf0ba-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="bf0ba-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="bf0ba-116">Un cliente que sale de un estado a otro debe volver al primero desde el segundo.</span><span class="sxs-lookup"><span data-stu-id="bf0ba-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="bf0ba-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf0ba-117">Description</span></span>

<span data-ttu-id="bf0ba-118">Durante este estado, el cliente actualiza el encabezado de un mensaje en un almacén local.</span><span class="sxs-lookup"><span data-stu-id="bf0ba-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="bf0ba-119">El almacén local entra en este estado en **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** y sale cuando se llama a **[IOSTX::SyncHdrEnd.](iostx-synchdrend.md)**</span><span class="sxs-lookup"><span data-stu-id="bf0ba-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="bf0ba-120">Durante este estado, Outlook inicializa los miembros de la estructura de datos **HDRSYNC** asociada con información sobre el encabezado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="bf0ba-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="bf0ba-121">El cliente primero descarga el elemento de mensaje completo del servidor y, a continuación, actualiza el encabezado del elemento de mensaje localmente.</span><span class="sxs-lookup"><span data-stu-id="bf0ba-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="bf0ba-122">Cuando finaliza la sincronización, el cliente establece los resultados de descarga.</span><span class="sxs-lookup"><span data-stu-id="bf0ba-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="bf0ba-123">El almacén local vuelve al estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="bf0ba-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bf0ba-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf0ba-124">See also</span></span>



[<span data-ttu-id="bf0ba-125">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="bf0ba-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="bf0ba-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="bf0ba-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="bf0ba-127">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="bf0ba-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="bf0ba-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="bf0ba-128">SYNCSTATE</span></span>](syncstate.md)

