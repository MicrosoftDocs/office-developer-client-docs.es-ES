---
title: Cargar estado de lectura de estado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 172eaf47d305cf6e4d1ba54ceb4ac4b4feab80e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820937"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="665a1-103">Cargar estado de lectura de estado</span><span class="sxs-lookup"><span data-stu-id="665a1-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="665a1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="665a1-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="665a1-105">En este tema se describe qué ocurre durante la carga leer el estado del estado de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="665a1-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="665a1-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="665a1-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="665a1-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="665a1-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="665a1-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="665a1-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="665a1-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="665a1-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="665a1-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="665a1-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="665a1-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="665a1-111">From this state:</span></span>  <br/> |[<span data-ttu-id="665a1-112">Cargar el estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="665a1-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="665a1-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="665a1-113">To this state:</span></span>  <br/> |<span data-ttu-id="665a1-114">Cargar el estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="665a1-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="665a1-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="665a1-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="665a1-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="665a1-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="665a1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="665a1-117">Description</span></span>

<span data-ttu-id="665a1-118">Este estado inicia carga el estado de lectura de elementos en una carpeta especificada en un estado de tabla de carga anterior.</span><span class="sxs-lookup"><span data-stu-id="665a1-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="665a1-119">Durante este estado, Outlook inicializa la estructura de datos **UPREAD** asociada con información para esos elementos en la carpeta cuyo estado de lectura ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="665a1-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="665a1-120">El cliente, a continuación, actualiza el estado de lectura de estos elementos en el servidor como leídos o no leídos.</span><span class="sxs-lookup"><span data-stu-id="665a1-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="665a1-121">Cuando finaliza este estado, Outlook borra la información interna sobre el estado de lectura del elemento, impide que el estado de lectura del elemento que se está cargando nuevamente.</span><span class="sxs-lookup"><span data-stu-id="665a1-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="665a1-122">Devuelve el almacén local en el estado de la tabla de carga.</span><span class="sxs-lookup"><span data-stu-id="665a1-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="665a1-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="665a1-123">See also</span></span>



[<span data-ttu-id="665a1-124">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="665a1-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="665a1-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="665a1-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="665a1-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="665a1-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="665a1-127">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="665a1-127">SYNCSTATE</span></span>](syncstate.md)

