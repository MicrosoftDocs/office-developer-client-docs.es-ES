---
title: Eliminar estado estado de carga
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ff957e649d5de64c65ac169b3bc413ac7b6c9491
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820934"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="7e100-103">Eliminar estado estado de carga</span><span class="sxs-lookup"><span data-stu-id="7e100-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="7e100-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e100-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="7e100-105">En este tema se describe qué ocurre durante la carga Eliminar estado de estado de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="7e100-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7e100-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="7e100-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e100-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="7e100-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="7e100-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="7e100-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="7e100-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="7e100-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="7e100-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="7e100-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="7e100-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="7e100-111">From this state:</span></span>  <br/> |[<span data-ttu-id="7e100-112">Cargar el estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="7e100-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="7e100-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="7e100-113">To this state:</span></span>  <br/> |<span data-ttu-id="7e100-114">Cargar el estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="7e100-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="7e100-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="7e100-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="7e100-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="7e100-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="7e100-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e100-117">Description</span></span>

<span data-ttu-id="7e100-118">Este estado inicia la actualización en un servidor de los elementos de Outlook (correo, calendario, contacto, tarea, nota o diario) que se han eliminado en una carpeta en un almacén local especificado en un estado de tabla de carga anterior.</span><span class="sxs-lookup"><span data-stu-id="7e100-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="7e100-119">Durante este estado, Outlook inicializa a los miembros de la estructura de datos **UPDEL** asociado con información para los elementos que se han eliminado o movido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="7e100-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="7e100-120">El cliente, a continuación, elimina los elementos especificados en la carpeta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="7e100-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="7e100-121">Para distinguir los elementos que se han movido en lugar de tener que se ha eliminado, el cliente debe comprobar a los miembros de *pupmov* identificados en la estructura **UPDEL** .</span><span class="sxs-lookup"><span data-stu-id="7e100-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="7e100-122">Cuando finaliza este estado, Outlook borra la información interna que indica que se ha eliminado el elemento; Por consiguiente, Outlook ya no tendrá un registro del elemento.</span><span class="sxs-lookup"><span data-stu-id="7e100-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="7e100-123">Devuelve el almacén local en el estado de la tabla de carga.</span><span class="sxs-lookup"><span data-stu-id="7e100-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e100-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="7e100-124">See also</span></span>



[<span data-ttu-id="7e100-125">Acerca de la API de replicación</span><span class="sxs-lookup"><span data-stu-id="7e100-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7e100-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7e100-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="7e100-127">Acerca de la máquina de estado de replicación</span><span class="sxs-lookup"><span data-stu-id="7e100-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7e100-128">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="7e100-128">SYNCSTATE</span></span>](syncstate.md)

