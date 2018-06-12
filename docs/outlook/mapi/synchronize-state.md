---
title: Sincronizar estado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 36bdeecfaaa94492b1e719dbd1cf455bfa40db47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820829"
---
# <a name="synchronize-state"></a><span data-ttu-id="4787c-103">Sincronizar estado</span><span class="sxs-lookup"><span data-stu-id="4787c-103">Synchronize State</span></span>

  
  
<span data-ttu-id="4787c-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4787c-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="4787c-105">En este tema se describe qué ocurre durante el estado de sincronización de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="4787c-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4787c-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4787c-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4787c-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="4787c-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4787c-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="4787c-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="4787c-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="4787c-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4787c-110">**[SINCRONIZACIÓN](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="4787c-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="4787c-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="4787c-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4787c-112">Estado de inactividad</span><span class="sxs-lookup"><span data-stu-id="4787c-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="4787c-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="4787c-113">To this state:</span></span>  <br/> |<span data-ttu-id="4787c-114">[Estado de la jerarquía de descarga](download-hierarchy-state.md), [sincronizar el estado del contenido](synchronize-contents-state.md), [cargar el estado de la jerarquía](upload-hierarchy-state.md)o estado inactivo</span><span class="sxs-lookup"><span data-stu-id="4787c-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4787c-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="4787c-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4787c-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="4787c-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4787c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4787c-117">Description</span></span>

<span data-ttu-id="4787c-118">Este estado inicia la sincronización.</span><span class="sxs-lookup"><span data-stu-id="4787c-118">This state initiates synchronization.</span></span> <span data-ttu-id="4787c-119">Puede realizar la transición de un almacén local a una carga o un estado de la descarga desde aquí.</span><span class="sxs-lookup"><span data-stu-id="4787c-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="4787c-120">Por ejemplo, puede mover un almacén local en el estado de la jerarquía de cargar para cargar una jerarquía de carpetas en el servidor, o puede realizar una sincronización completa por primera carga la jerarquía y, a continuación, descarga la jerarquía desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="4787c-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="4787c-121">Durante este estado, Outlook inicializa la estructura de datos de **sincronización** asociada con la ruta de acceso en el almacén local, por lo que Outlook ve modificaciones durante otros Estados.</span><span class="sxs-lookup"><span data-stu-id="4787c-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="4787c-122">El cliente establece el [in] los miembros de **sincronización**, que indica cómo controlar otros Estados de Outlook.</span><span class="sxs-lookup"><span data-stu-id="4787c-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="4787c-123">Por ejemplo, el cliente puede establecer *ulFlags* en **UPS_UPLOAD_ONLY** y **UPS_THESE_FOLDERS** y se cargará *pel* a una lista de identificadores de entrada de las carpetas para indicar a Outlook que sólo estas carpetas.</span><span class="sxs-lookup"><span data-stu-id="4787c-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="4787c-124">Cuando finaliza este estado, el almacén local vuelve al estado inactivo.</span><span class="sxs-lookup"><span data-stu-id="4787c-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4787c-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="4787c-125">See also</span></span>



[<span data-ttu-id="4787c-126">Acerca de la API de replicación</span><span class="sxs-lookup"><span data-stu-id="4787c-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4787c-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="4787c-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4787c-128">Acerca de la máquina de estado de replicación</span><span class="sxs-lookup"><span data-stu-id="4787c-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4787c-129">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="4787c-129">SYNCSTATE</span></span>](syncstate.md)

