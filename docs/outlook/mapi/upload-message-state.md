---
title: Upload Estado del mensaje
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433804"
---
# <a name="upload-message-state"></a><span data-ttu-id="f8acd-103">Upload Estado del mensaje</span><span class="sxs-lookup"><span data-stu-id="f8acd-103">Upload Message State</span></span>

  
  
<span data-ttu-id="f8acd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8acd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="f8acd-105">En este tema se describe lo que sucede durante el estado del mensaje de carga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="f8acd-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f8acd-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="f8acd-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8acd-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="f8acd-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="f8acd-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="f8acd-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="f8acd-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="f8acd-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="f8acd-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="f8acd-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="f8acd-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="f8acd-111">From this state:</span></span>  <br/> |[<span data-ttu-id="f8acd-112">Upload de tabla</span><span class="sxs-lookup"><span data-stu-id="f8acd-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="f8acd-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="f8acd-113">To this state:</span></span>  <br/> |<span data-ttu-id="f8acd-114">Upload de tabla</span><span class="sxs-lookup"><span data-stu-id="f8acd-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="f8acd-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="f8acd-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="f8acd-116">Un cliente que sale de un estado a otro debe volver al primero desde el segundo.</span><span class="sxs-lookup"><span data-stu-id="f8acd-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="f8acd-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8acd-117">Description</span></span>

<span data-ttu-id="f8acd-118">Este estado inicia la carga de un elemento Outlook (correo, calendario, contacto, tarea, nota o diario) que es nuevo o que se ha movido a la carpeta actual o que se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="f8acd-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="f8acd-119">Outlook inicializa la estructura de datos **UPMSG** correpsonding con la información adecuada para el elemento que se va a agregar, mover o modificar.</span><span class="sxs-lookup"><span data-stu-id="f8acd-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="f8acd-120">Si el elemento se ha agregado o movido, el cliente agrega o actualiza correctamente el elemento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f8acd-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="f8acd-121">Si el elemento se ha modificado, Outlook especifica aún más en la estructura de datos **UPMSG** si las modificaciones están en un encabezado de mensaje (en cuyo caso el elemento es el encabezado del mensaje), en las propiedades del elemento o en el propio elemento que requiere resolución de conflictos.</span><span class="sxs-lookup"><span data-stu-id="f8acd-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="f8acd-122">A continuación, el cliente actualiza el elemento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="f8acd-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="f8acd-123">Cuando finaliza la carga del elemento, Outlook indica que el mensaje se ha cargado, de modo que no se procesará en una carga posterior.</span><span class="sxs-lookup"><span data-stu-id="f8acd-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="f8acd-124">El almacén local vuelve al estado de la tabla de carga.</span><span class="sxs-lookup"><span data-stu-id="f8acd-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f8acd-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8acd-125">See also</span></span>



[<span data-ttu-id="f8acd-126">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="f8acd-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="f8acd-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f8acd-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f8acd-128">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="f8acd-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="f8acd-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="f8acd-129">SYNCSTATE</span></span>](syncstate.md)

