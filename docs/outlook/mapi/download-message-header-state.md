---
title: Estado del encabezado de mensaje de descarga
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 7407b6606634ecc0151f582e4481ecbff5e7dc57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816705"
---
# <a name="download-message-header-state"></a><span data-ttu-id="6a18f-103">Estado del encabezado de mensaje de descarga</span><span class="sxs-lookup"><span data-stu-id="6a18f-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="6a18f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6a18f-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="6a18f-105">En este tema se describe qué ocurre durante el estado del encabezado de mensaje de descarga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="6a18f-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="6a18f-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="6a18f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a18f-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="6a18f-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="6a18f-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="6a18f-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="6a18f-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="6a18f-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="6a18f-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="6a18f-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="6a18f-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="6a18f-111">From this state:</span></span>  <br/> |[<span data-ttu-id="6a18f-112">Estado de inactividad</span><span class="sxs-lookup"><span data-stu-id="6a18f-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="6a18f-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="6a18f-113">To this state:</span></span>  <br/> |<span data-ttu-id="6a18f-114">Estado de inactividad</span><span class="sxs-lookup"><span data-stu-id="6a18f-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="6a18f-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="6a18f-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="6a18f-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="6a18f-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="6a18f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a18f-117">Description</span></span>

<span data-ttu-id="6a18f-118">Durante este estado, el cliente actualiza el encabezado de un mensaje en un almacén local.</span><span class="sxs-lookup"><span data-stu-id="6a18f-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="6a18f-119">El almacén local entra en este estado después de **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** y se cierra cuando se llama a **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** .</span><span class="sxs-lookup"><span data-stu-id="6a18f-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="6a18f-120">Durante este estado, Outlook inicializa a los miembros de la estructura de datos **HDRSYNC** asociado con información sobre el encabezado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="6a18f-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="6a18f-121">El cliente descarga primero el elemento de mensaje completo desde el servidor y, a continuación, actualiza el encabezado del elemento de mensaje localmente.</span><span class="sxs-lookup"><span data-stu-id="6a18f-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="6a18f-122">Cuando finaliza la sincronización, el cliente establece los resultados de la descarga.</span><span class="sxs-lookup"><span data-stu-id="6a18f-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="6a18f-123">El almacén local se devuelve al estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="6a18f-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a18f-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="6a18f-124">See also</span></span>



[<span data-ttu-id="6a18f-125">Acerca de la API de replicación</span><span class="sxs-lookup"><span data-stu-id="6a18f-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="6a18f-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="6a18f-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="6a18f-127">Acerca de la máquina de estado de replicación</span><span class="sxs-lookup"><span data-stu-id="6a18f-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="6a18f-128">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="6a18f-128">SYNCSTATE</span></span>](syncstate.md)

