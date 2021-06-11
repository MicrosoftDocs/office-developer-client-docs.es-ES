---
title: Descargar estado de tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338342"
---
# <a name="download-table-state"></a><span data-ttu-id="b6b41-103">Descargar estado de tabla</span><span class="sxs-lookup"><span data-stu-id="b6b41-103">Download Table State</span></span>

  
  
<span data-ttu-id="b6b41-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6b41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b6b41-105">En este tema se describe lo que sucede durante el estado de la tabla de descarga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="b6b41-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b6b41-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b6b41-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6b41-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="b6b41-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="b6b41-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="b6b41-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="b6b41-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="b6b41-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="b6b41-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="b6b41-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="b6b41-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="b6b41-111">From this state:</span></span>  <br/> |[<span data-ttu-id="b6b41-112">Sincronizar el estado de contenido</span><span class="sxs-lookup"><span data-stu-id="b6b41-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="b6b41-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="b6b41-113">To this state:</span></span>  <br/> |<span data-ttu-id="b6b41-114">Sincronizar el estado de contenido</span><span class="sxs-lookup"><span data-stu-id="b6b41-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b6b41-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="b6b41-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="b6b41-116">Un cliente que sale de un estado a otro debe volver al primero desde el segundo.</span><span class="sxs-lookup"><span data-stu-id="b6b41-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="b6b41-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6b41-117">Description</span></span>

<span data-ttu-id="b6b41-118">Este estado inicia la descarga de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b6b41-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="b6b41-119">Durante este estado, Outlook inicializa la estructura de datos **de DNTBL** asociada con información sobre la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b6b41-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="b6b41-120">El cliente descarga el contenido de la carpeta y actualiza la carpeta en el almacén local con nuevos contenidos, modificaciones o eliminaciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="b6b41-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="b6b41-121">El proceso de descarga adopta Microsoft Exchange sincronización incremental de cambios (ICS).</span><span class="sxs-lookup"><span data-stu-id="b6b41-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="b6b41-122">Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b6b41-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="b6b41-123">Cuando finaliza este estado, el almacén local vuelve al estado de sincronización de contenido.</span><span class="sxs-lookup"><span data-stu-id="b6b41-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6b41-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6b41-124">See also</span></span>



[<span data-ttu-id="b6b41-125">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="b6b41-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b6b41-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b41-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b6b41-127">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="b6b41-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b6b41-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="b6b41-128">SYNCSTATE</span></span>](syncstate.md)

