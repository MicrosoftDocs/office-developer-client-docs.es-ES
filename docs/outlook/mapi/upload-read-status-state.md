---
title: Cargar estado de lectura
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431543"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="9b105-103">Cargar estado de lectura</span><span class="sxs-lookup"><span data-stu-id="9b105-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="9b105-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b105-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9b105-105">En este tema se describe lo que sucede durante el estado de lectura de carga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="9b105-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9b105-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9b105-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b105-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="9b105-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="9b105-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="9b105-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="9b105-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="9b105-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="9b105-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="9b105-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="9b105-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="9b105-111">From this state:</span></span>  <br/> |[<span data-ttu-id="9b105-112">Cargar el estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="9b105-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="9b105-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="9b105-113">To this state:</span></span>  <br/> |<span data-ttu-id="9b105-114">Cargar el estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="9b105-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="9b105-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="9b105-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="9b105-116">Un cliente que va de un estado a otro debe volver al primero desde el segundo.</span><span class="sxs-lookup"><span data-stu-id="9b105-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="9b105-117">Description</span><span class="sxs-lookup"><span data-stu-id="9b105-117">Description</span></span>

<span data-ttu-id="9b105-118">Este estado inicia la carga del estado de lectura de los elementos de una carpeta especificada en un estado de tabla de carga anterior.</span><span class="sxs-lookup"><span data-stu-id="9b105-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="9b105-119">Durante este estado, Outlook inicializa la estructura de datos **UPREAD** asociada con información de los elementos de la carpeta cuyo estado de lectura ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9b105-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="9b105-120">A continuación, el cliente actualiza el estado de lectura de estos elementos en el servidor como leídos o no leídos.</span><span class="sxs-lookup"><span data-stu-id="9b105-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="9b105-121">Cuando finaliza este estado, Outlook borra la información interna sobre el estado de lectura del elemento, evitando que el estado de lectura del elemento vuelva a cargarse.</span><span class="sxs-lookup"><span data-stu-id="9b105-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="9b105-122">El almacén local vuelve al estado de la tabla de carga.</span><span class="sxs-lookup"><span data-stu-id="9b105-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b105-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9b105-123">See also</span></span>



[<span data-ttu-id="9b105-124">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="9b105-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9b105-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9b105-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9b105-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="9b105-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9b105-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="9b105-127">SYNCSTATE</span></span>](syncstate.md)

