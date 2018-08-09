---
title: Cargar estado de la jerarquía
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d53790cb51b660c781190cf41ca317c823a021e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820940"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="1284b-103">Cargar estado de la jerarquía</span><span class="sxs-lookup"><span data-stu-id="1284b-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="1284b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1284b-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="1284b-105">En este tema se describe qué ocurre durante el estado de la jerarquía de carga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="1284b-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="1284b-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="1284b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1284b-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="1284b-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="1284b-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="1284b-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="1284b-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="1284b-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="1284b-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="1284b-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="1284b-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="1284b-111">From this state:</span></span>  <br/> |[<span data-ttu-id="1284b-112">Sincronizar estado</span><span class="sxs-lookup"><span data-stu-id="1284b-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="1284b-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="1284b-113">To this state:</span></span>  <br/> |<span data-ttu-id="1284b-114">[Cargar el estado de la carpeta](upload-folder-state.md), o sincronizar estado</span><span class="sxs-lookup"><span data-stu-id="1284b-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="1284b-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="1284b-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="1284b-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="1284b-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="1284b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1284b-117">Description</span></span>

<span data-ttu-id="1284b-118">Este estado inicia la carga de una jerarquía de árbol de la carpeta que se ha especificado en una anterior sincronizar estado.</span><span class="sxs-lookup"><span data-stu-id="1284b-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="1284b-119">Outlook determina el número de carpetas que se han creado o modificado en esa jerarquía e inicializa *cEnt* en **UPHIER**.</span><span class="sxs-lookup"><span data-stu-id="1284b-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="1284b-120">Outlook también mantiene un recuento del número de carpetas que se cargan con otro miembro *iEnt* .</span><span class="sxs-lookup"><span data-stu-id="1284b-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="1284b-121">Para cargar cada una de las carpetas *cEnt* , el cliente mueve el almacén local en el estado de la carpeta de carga, cuando finaliza la carga de la carpeta de nuevo en el estado de la jerarquía de carga.</span><span class="sxs-lookup"><span data-stu-id="1284b-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="1284b-122">Cuando finaliza el estado de la jerarquía de carga, el almacén local se devuelve en el estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="1284b-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1284b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1284b-123">See also</span></span>



[<span data-ttu-id="1284b-124">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="1284b-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="1284b-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="1284b-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="1284b-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="1284b-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="1284b-127">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="1284b-127">SYNCSTATE</span></span>](syncstate.md)

