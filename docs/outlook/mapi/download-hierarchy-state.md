---
title: Descargar estado de jerarquía
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337012"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="6cdc9-103">Descargar estado de jerarquía</span><span class="sxs-lookup"><span data-stu-id="6cdc9-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="6cdc9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cdc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="6cdc9-105">En este tema se describe lo que sucede durante el estado de jerarquía de descarga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="6cdc9-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="6cdc9-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="6cdc9-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6cdc9-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="6cdc9-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="6cdc9-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="6cdc9-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="6cdc9-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="6cdc9-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="6cdc9-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="6cdc9-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="6cdc9-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="6cdc9-111">From this state:</span></span>  <br/> |[<span data-ttu-id="6cdc9-112">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="6cdc9-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="6cdc9-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="6cdc9-113">To this state:</span></span>  <br/> |<span data-ttu-id="6cdc9-114">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="6cdc9-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="6cdc9-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="6cdc9-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="6cdc9-116">Un cliente que sale de un estado a otro debe volver al primero desde el segundo.</span><span class="sxs-lookup"><span data-stu-id="6cdc9-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="6cdc9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cdc9-117">Description</span></span>

<span data-ttu-id="6cdc9-118">Este estado inicia la descarga de una jerarquía de árbol de carpetas de un servidor al almacén local.</span><span class="sxs-lookup"><span data-stu-id="6cdc9-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="6cdc9-119">Outlook inicializa la estructura de datos **DNHIER** asociada con un puntero a la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="6cdc9-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="6cdc9-120">El cliente descarga la jerarquía e inserta nuevas carpetas o modificaciones en las carpetas del almacén local.</span><span class="sxs-lookup"><span data-stu-id="6cdc9-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="6cdc9-121">El proceso de descarga adopta Microsoft Exchange sincronización incremental de cambios (ICS).</span><span class="sxs-lookup"><span data-stu-id="6cdc9-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="6cdc9-122">Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="6cdc9-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="6cdc9-123">Cuando finaliza este estado, el almacén local vuelve al estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="6cdc9-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6cdc9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6cdc9-124">See also</span></span>



[<span data-ttu-id="6cdc9-125">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="6cdc9-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="6cdc9-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="6cdc9-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="6cdc9-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="6cdc9-127">SYNCSTATE</span></span>](syncstate.md)

