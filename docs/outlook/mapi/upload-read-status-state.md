---
title: Cargar estado de lectura de estado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282666"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="2cf71-103">Cargar estado de lectura de estado</span><span class="sxs-lookup"><span data-stu-id="2cf71-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="2cf71-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cf71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2cf71-105">En este tema se describe lo que ocurre durante el estado de lectura de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="2cf71-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2cf71-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="2cf71-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2cf71-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="2cf71-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="2cf71-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="2cf71-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="2cf71-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="2cf71-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="2cf71-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="2cf71-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="2cf71-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="2cf71-111">From this state:</span></span>  <br/> |[<span data-ttu-id="2cf71-112">Cargar estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="2cf71-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="2cf71-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="2cf71-113">To this state:</span></span>  <br/> |<span data-ttu-id="2cf71-114">Cargar estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="2cf71-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="2cf71-115">La máquina de estado de replicación es un equipo de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="2cf71-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="2cf71-116">Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda.</span><span class="sxs-lookup"><span data-stu-id="2cf71-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="2cf71-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cf71-117">Description</span></span>

<span data-ttu-id="2cf71-118">Este estado inicia la carga del estado de lectura de los elementos en una carpeta especificada en un estado de tabla de carga anterior.</span><span class="sxs-lookup"><span data-stu-id="2cf71-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="2cf71-119">Durante este estado, Outlook inicializa la estructura de datos de **lectura** asociada con la información de los elementos en la carpeta cuyo estado de lectura ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="2cf71-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="2cf71-120">A continuación, el cliente actualiza el estado de lectura de estos elementos en el servidor como leídos o no leídos.</span><span class="sxs-lookup"><span data-stu-id="2cf71-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="2cf71-121">Cuando finaliza este estado, Outlook borra la información interna sobre el estado de lectura del elemento, lo que evita que se vuelva a cargar el estado de lectura del elemento.</span><span class="sxs-lookup"><span data-stu-id="2cf71-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="2cf71-122">El almacén local vuelve al estado cargar tabla.</span><span class="sxs-lookup"><span data-stu-id="2cf71-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2cf71-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cf71-123">See also</span></span>



[<span data-ttu-id="2cf71-124">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="2cf71-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2cf71-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="2cf71-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2cf71-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="2cf71-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2cf71-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="2cf71-127">SYNCSTATE</span></span>](syncstate.md)

