---
title: Descargar estado de la tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e75407f62a7e6440f6c8dca8c1d2c76843048da4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595401"
---
# <a name="download-table-state"></a><span data-ttu-id="3ca03-103">Descargar estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="3ca03-103">Download Table State</span></span>

  
  
<span data-ttu-id="3ca03-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ca03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3ca03-105">En este tema se describe qué ocurre durante el estado de la tabla de descarga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="3ca03-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3ca03-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="3ca03-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ca03-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="3ca03-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="3ca03-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="3ca03-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="3ca03-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="3ca03-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="3ca03-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="3ca03-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="3ca03-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="3ca03-111">From this state:</span></span>  <br/> |[<span data-ttu-id="3ca03-112">Sincronizar el estado del contenido</span><span class="sxs-lookup"><span data-stu-id="3ca03-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="3ca03-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="3ca03-113">To this state:</span></span>  <br/> |<span data-ttu-id="3ca03-114">Sincronizar el estado del contenido</span><span class="sxs-lookup"><span data-stu-id="3ca03-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3ca03-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="3ca03-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="3ca03-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="3ca03-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="3ca03-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ca03-117">Description</span></span>

<span data-ttu-id="3ca03-118">Este estado inicia la descarga de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="3ca03-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="3ca03-119">Durante este estado, Outlook inicializa la estructura de datos **DNTBL** asociada con información acerca de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="3ca03-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="3ca03-120">El cliente descarga el contenido de la carpeta y actualiza la carpeta en el almacén local con contenido nuevo, modificaciones o eliminaciones desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="3ca03-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="3ca03-121">El proceso de descarga adopta la sincronización de cambio Incremental (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="3ca03-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="3ca03-122">Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ca03-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="3ca03-123">Cuando finaliza este estado, se devuelve el almacén local en el estado del contenido de sincronizar.</span><span class="sxs-lookup"><span data-stu-id="3ca03-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ca03-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3ca03-124">See also</span></span>



[<span data-ttu-id="3ca03-125">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="3ca03-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3ca03-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3ca03-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3ca03-127">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="3ca03-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3ca03-128">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="3ca03-128">SYNCSTATE</span></span>](syncstate.md)

