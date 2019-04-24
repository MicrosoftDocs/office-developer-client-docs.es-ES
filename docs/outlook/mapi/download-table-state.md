---
title: Descargar estado de la tabla
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
# <a name="download-table-state"></a><span data-ttu-id="762b4-103">Descargar estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="762b4-103">Download Table State</span></span>

  
  
<span data-ttu-id="762b4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="762b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="762b4-105">En este tema se describe lo que ocurre durante el estado de la tabla de descarga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="762b4-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="762b4-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="762b4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="762b4-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="762b4-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="762b4-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="762b4-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="762b4-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="762b4-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="762b4-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="762b4-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="762b4-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="762b4-111">From this state:</span></span>  <br/> |[<span data-ttu-id="762b4-112">Estado de sincronización de contenido</span><span class="sxs-lookup"><span data-stu-id="762b4-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="762b4-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="762b4-113">To this state:</span></span>  <br/> |<span data-ttu-id="762b4-114">Estado de sincronización de contenido</span><span class="sxs-lookup"><span data-stu-id="762b4-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="762b4-115">La máquina de estado de replicación es un equipo de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="762b4-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="762b4-116">Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda.</span><span class="sxs-lookup"><span data-stu-id="762b4-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="762b4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="762b4-117">Description</span></span>

<span data-ttu-id="762b4-118">Este estado inicia la descarga de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="762b4-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="762b4-119">Durante este estado, Outlook inicializa la estructura de datos **DNTBL** asociada con la información acerca de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="762b4-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="762b4-120">El cliente descarga el contenido de la carpeta y actualiza la carpeta en el almacén local con nuevo contenido, modificaciones o eliminaciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="762b4-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="762b4-121">El proceso de descarga adopta la sincronización de cambio incremental (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="762b4-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="762b4-122">Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="762b4-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="762b4-123">Cuando finaliza este estado, el almacén local vuelve al estado Synchronize Contents.</span><span class="sxs-lookup"><span data-stu-id="762b4-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="762b4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="762b4-124">See also</span></span>



[<span data-ttu-id="762b4-125">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="762b4-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="762b4-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="762b4-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="762b4-127">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="762b4-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="762b4-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="762b4-128">SYNCSTATE</span></span>](syncstate.md)

