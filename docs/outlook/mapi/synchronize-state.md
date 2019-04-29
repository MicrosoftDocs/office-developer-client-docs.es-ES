---
title: Estado de sincronización
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414630"
---
# <a name="synchronize-state"></a><span data-ttu-id="b8684-103">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="b8684-103">Synchronize State</span></span>

  
  
<span data-ttu-id="b8684-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8684-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b8684-105">En este tema se describe lo que ocurre durante el estado de sincronización de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="b8684-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b8684-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b8684-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8684-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="b8684-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="b8684-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="b8684-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="b8684-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="b8684-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="b8684-110">**[SINCRONIZÁNDOSE](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="b8684-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="b8684-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="b8684-111">From this state:</span></span>  <br/> |[<span data-ttu-id="b8684-112">Estado inactivo</span><span class="sxs-lookup"><span data-stu-id="b8684-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="b8684-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="b8684-113">To this state:</span></span>  <br/> |<span data-ttu-id="b8684-114">[Descargar estado de jerarquía](download-hierarchy-state.md), [sincronizar estado de contenido](synchronize-contents-state.md), cargar estado de [jerarquía](upload-hierarchy-state.md)o estado de inactividad</span><span class="sxs-lookup"><span data-stu-id="b8684-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b8684-115">La máquina de estado de replicación es un equipo de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="b8684-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="b8684-116">Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda.</span><span class="sxs-lookup"><span data-stu-id="b8684-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="b8684-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8684-117">Description</span></span>

<span data-ttu-id="b8684-118">Este estado inicia la sincronización.</span><span class="sxs-lookup"><span data-stu-id="b8684-118">This state initiates synchronization.</span></span> <span data-ttu-id="b8684-119">Un almacén local puede realizar la transición a un estado de carga o descarga desde aquí.</span><span class="sxs-lookup"><span data-stu-id="b8684-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="b8684-120">Por ejemplo, un almacén local puede pasar al estado de carga de la jerarquía para cargar una jerarquía de carpetas en el servidor, o puede realizar una sincronización completa recargando primero la jerarquía y, a continuación, descargando la jerarquía desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="b8684-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="b8684-121">Durante este estado, Outlook inicializa la estructura de datos de **sincronización** asociada con la ruta de acceso al almacén local, por lo que Outlook ve las modificaciones durante otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b8684-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="b8684-122">El cliente establece los miembros de **sincronización**[in], que indican a Outlook cómo controlar otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b8684-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="b8684-123">Por ejemplo, el cliente puede establecer *ulFlags* en **UPS_UPLOAD_ONLY** y **UPS_THESE_FOLDERS** y *PEL* en una lista de identificadores de entrada de las carpetas para decir a Outlook que solo se cargarán estas carpetas.</span><span class="sxs-lookup"><span data-stu-id="b8684-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="b8684-124">Cuando finaliza este estado, el almacén local vuelve al estado inactivo.</span><span class="sxs-lookup"><span data-stu-id="b8684-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b8684-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="b8684-125">See also</span></span>



[<span data-ttu-id="b8684-126">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="b8684-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b8684-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b8684-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b8684-128">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="b8684-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b8684-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="b8684-129">SYNCSTATE</span></span>](syncstate.md)

