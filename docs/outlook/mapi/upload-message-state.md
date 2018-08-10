---
title: Cargar estado de los mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 752756cbcf6c1ce487188dd4b9ba55eee6506cd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820935"
---
# <a name="upload-message-state"></a><span data-ttu-id="b46b4-103">Cargar estado de los mensajes</span><span class="sxs-lookup"><span data-stu-id="b46b4-103">Upload Message State</span></span>

  
  
<span data-ttu-id="b46b4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b46b4-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="b46b4-105">En este tema se describe qué ocurre durante el estado del mensaje de carga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="b46b4-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b46b4-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b46b4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b46b4-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="b46b4-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="b46b4-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="b46b4-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="b46b4-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="b46b4-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="b46b4-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="b46b4-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="b46b4-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="b46b4-111">From this state:</span></span>  <br/> |[<span data-ttu-id="b46b4-112">Cargar el estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="b46b4-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="b46b4-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="b46b4-113">To this state:</span></span>  <br/> |<span data-ttu-id="b46b4-114">Cargar el estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="b46b4-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b46b4-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="b46b4-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="b46b4-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="b46b4-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="b46b4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b46b4-117">Description</span></span>

<span data-ttu-id="b46b4-118">Este estado inicia la carga de un elemento de Outlook (correo, calendario, contacto, tarea, nota o diario) que es nuevo o se ha movido a la carpeta actual, o que han sido modificado.</span><span class="sxs-lookup"><span data-stu-id="b46b4-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="b46b4-119">Outlook inicializa la estructura de datos **UPMSG** de correpsonding con la información apropiada para el elemento, tal y como se agrega, mueve o modifica.</span><span class="sxs-lookup"><span data-stu-id="b46b4-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="b46b4-120">Si el elemento se ha agregado o movido, el cliente, a continuación, adecuadamente agrega o actualiza el elemento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b46b4-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="b46b4-121">Si el elemento se ha modificado, Outlook aún más especifica en la estructura de datos **UPMSG** si las modificaciones están en un encabezado de mensaje (en cuyo caso el elemento es el encabezado del mensaje), en las propiedades de elemento o en el propio elemento que requiere el conflicto resolución.</span><span class="sxs-lookup"><span data-stu-id="b46b4-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="b46b4-122">El cliente, a continuación, actualiza el elemento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b46b4-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="b46b4-123">Cuando finaliza la carga de elemento, Outlook notas que el mensaje se ha cargado, por lo que no se procesarán en una carga posterior.</span><span class="sxs-lookup"><span data-stu-id="b46b4-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="b46b4-124">Devuelve el almacén local en el estado de la tabla de carga.</span><span class="sxs-lookup"><span data-stu-id="b46b4-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b46b4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b46b4-125">See also</span></span>



[<span data-ttu-id="b46b4-126">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="b46b4-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b46b4-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b46b4-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b46b4-128">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="b46b4-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b46b4-129">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="b46b4-129">SYNCSTATE</span></span>](syncstate.md)
