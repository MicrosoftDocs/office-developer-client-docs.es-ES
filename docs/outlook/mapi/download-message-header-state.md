---
title: Descargar estado del encabezado del mensaje
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338839"
---
# <a name="download-message-header-state"></a><span data-ttu-id="6a2bf-103">Descargar estado del encabezado del mensaje</span><span class="sxs-lookup"><span data-stu-id="6a2bf-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="6a2bf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a2bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="6a2bf-105">En este tema se describe lo que ocurre durante el estado de encabezado del mensaje de descarga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="6a2bf-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="6a2bf-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="6a2bf-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a2bf-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="6a2bf-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="6a2bf-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="6a2bf-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="6a2bf-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="6a2bf-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="6a2bf-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="6a2bf-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="6a2bf-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="6a2bf-111">From this state:</span></span>  <br/> |[<span data-ttu-id="6a2bf-112">Estado inactivo</span><span class="sxs-lookup"><span data-stu-id="6a2bf-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="6a2bf-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="6a2bf-113">To this state:</span></span>  <br/> |<span data-ttu-id="6a2bf-114">Estado inactivo</span><span class="sxs-lookup"><span data-stu-id="6a2bf-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="6a2bf-115">La máquina de estado de replicación es un equipo de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="6a2bf-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="6a2bf-116">Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda.</span><span class="sxs-lookup"><span data-stu-id="6a2bf-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="6a2bf-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a2bf-117">Description</span></span>

<span data-ttu-id="6a2bf-118">Durante este estado, el cliente actualiza el encabezado de un mensaje en un almacén local.</span><span class="sxs-lookup"><span data-stu-id="6a2bf-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="6a2bf-119">El almacén local especifica este estado a partir de **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** y sale cuando se llama a **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** .</span><span class="sxs-lookup"><span data-stu-id="6a2bf-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="6a2bf-120">Durante este estado, Outlook inicializa los miembros de la estructura de datos **HDRSYNC** asociada con la información sobre el encabezado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="6a2bf-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="6a2bf-121">En primer lugar, el cliente descarga el elemento de mensaje completo desde el servidor y, a continuación, actualiza el encabezado del elemento de mensaje de forma local.</span><span class="sxs-lookup"><span data-stu-id="6a2bf-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="6a2bf-122">Cuando finaliza sincronización, el cliente establece los resultados de la descarga.</span><span class="sxs-lookup"><span data-stu-id="6a2bf-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="6a2bf-123">El almacén local vuelve al estado inactivo.</span><span class="sxs-lookup"><span data-stu-id="6a2bf-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a2bf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a2bf-124">See also</span></span>



[<span data-ttu-id="6a2bf-125">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="6a2bf-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="6a2bf-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="6a2bf-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="6a2bf-127">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="6a2bf-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="6a2bf-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="6a2bf-128">SYNCSTATE</span></span>](syncstate.md)

