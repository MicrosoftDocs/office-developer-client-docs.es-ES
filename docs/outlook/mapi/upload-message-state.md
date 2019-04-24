---
title: Cargar estado del mensaje
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332637"
---
# <a name="upload-message-state"></a><span data-ttu-id="3cc65-103">Cargar estado del mensaje</span><span class="sxs-lookup"><span data-stu-id="3cc65-103">Upload Message State</span></span>

  
  
<span data-ttu-id="3cc65-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cc65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3cc65-105">En este tema se describe lo que ocurre durante el estado de carga del equipo de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="3cc65-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3cc65-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="3cc65-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3cc65-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="3cc65-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="3cc65-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="3cc65-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="3cc65-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="3cc65-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="3cc65-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="3cc65-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="3cc65-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="3cc65-111">From this state:</span></span>  <br/> |[<span data-ttu-id="3cc65-112">Cargar estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="3cc65-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="3cc65-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="3cc65-113">To this state:</span></span>  <br/> |<span data-ttu-id="3cc65-114">Cargar estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="3cc65-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3cc65-115">La máquina de estado de replicación es un equipo de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="3cc65-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="3cc65-116">Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda.</span><span class="sxs-lookup"><span data-stu-id="3cc65-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="3cc65-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cc65-117">Description</span></span>

<span data-ttu-id="3cc65-118">Este estado inicia la carga de un elemento de Outlook (correo, calendario, contacto, tarea, nota o diario) que es nuevo o se ha movido a la carpeta actual o que se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="3cc65-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="3cc65-119">Outlook inicializa la estructura de datos correpsonding **UPMSG** con la información adecuada para que el elemento se agregue, mueva o modifique.</span><span class="sxs-lookup"><span data-stu-id="3cc65-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="3cc65-120">Si se ha agregado o movido el elemento, el cliente, a continuación, agrega o actualiza correctamente el elemento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3cc65-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="3cc65-121">Si el elemento se ha modificado, Outlook especifica aún más la estructura de datos **UPMSG** si las modificaciones están en un encabezado de mensaje (en cuyo caso el elemento es el encabezado del mensaje), en las propiedades del elemento o en el propio elemento que requiere un conflicto. n.</span><span class="sxs-lookup"><span data-stu-id="3cc65-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="3cc65-122">A continuación, el cliente actualiza el elemento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3cc65-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="3cc65-123">Cuando finaliza el envío del elemento, Outlook indica que el mensaje se ha cargado para que no se procese en una carga posterior.</span><span class="sxs-lookup"><span data-stu-id="3cc65-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="3cc65-124">El almacén local vuelve al estado cargar tabla.</span><span class="sxs-lookup"><span data-stu-id="3cc65-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3cc65-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cc65-125">See also</span></span>



[<span data-ttu-id="3cc65-126">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="3cc65-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3cc65-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3cc65-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3cc65-128">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="3cc65-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3cc65-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="3cc65-129">SYNCSTATE</span></span>](syncstate.md)

