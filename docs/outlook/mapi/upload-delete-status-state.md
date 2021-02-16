---
title: Cargar estado de eliminación
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425844"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="4e65e-103">Cargar estado de eliminación</span><span class="sxs-lookup"><span data-stu-id="4e65e-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="4e65e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e65e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4e65e-105">En este tema se describe lo que sucede durante el estado de eliminación de carga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="4e65e-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4e65e-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4e65e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e65e-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="4e65e-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4e65e-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="4e65e-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="4e65e-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="4e65e-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4e65e-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="4e65e-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="4e65e-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="4e65e-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4e65e-112">Cargar el estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="4e65e-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="4e65e-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="4e65e-113">To this state:</span></span>  <br/> |<span data-ttu-id="4e65e-114">Cargar el estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="4e65e-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4e65e-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="4e65e-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4e65e-116">Un cliente que va de un estado a otro debe volver al primero desde el segundo.</span><span class="sxs-lookup"><span data-stu-id="4e65e-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4e65e-117">Description</span><span class="sxs-lookup"><span data-stu-id="4e65e-117">Description</span></span>

<span data-ttu-id="4e65e-118">Este estado inicia la actualización en un servidor de los elementos de Outlook (correo, calendario, contacto, tarea, nota o diario) que se han eliminado en una carpeta de un almacén local especificado en un estado de tabla de carga anterior.</span><span class="sxs-lookup"><span data-stu-id="4e65e-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="4e65e-119">Durante este estado, Outlook inicializa los miembros de la estructura de datos **UPDEL** asociada con información de los elementos que se han eliminado o movido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4e65e-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="4e65e-120">A continuación, el cliente elimina los elementos especificados en la carpeta del servidor.</span><span class="sxs-lookup"><span data-stu-id="4e65e-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="4e65e-121">Para distinguir los elementos que se han movido en lugar de eliminarse, el cliente debe comprobar los miembros *demovmov* identificados en la **estructura UPDEL.**</span><span class="sxs-lookup"><span data-stu-id="4e65e-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="4e65e-122">Cuando finaliza este estado, Outlook borra la información interna que indica que el elemento se ha eliminado; por lo tanto, Outlook ya no tendrá un registro del elemento.</span><span class="sxs-lookup"><span data-stu-id="4e65e-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="4e65e-123">El almacén local vuelve al estado de la tabla de carga.</span><span class="sxs-lookup"><span data-stu-id="4e65e-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e65e-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4e65e-124">See also</span></span>



[<span data-ttu-id="4e65e-125">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="4e65e-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4e65e-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="4e65e-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4e65e-127">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="4e65e-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4e65e-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="4e65e-128">SYNCSTATE</span></span>](syncstate.md)

