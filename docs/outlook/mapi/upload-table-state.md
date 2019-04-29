---
title: Cargar estado de la tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405824"
---
# <a name="upload-table-state"></a><span data-ttu-id="4c823-103">Cargar estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="4c823-103">Upload Table State</span></span>

  
  
<span data-ttu-id="4c823-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c823-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4c823-105">En este tema se describe lo que sucede durante el estado de carga de la tabla de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="4c823-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4c823-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="4c823-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c823-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="4c823-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4c823-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="4c823-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="4c823-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="4c823-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4c823-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="4c823-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="4c823-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="4c823-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4c823-112">Estado de sincronización de contenido</span><span class="sxs-lookup"><span data-stu-id="4c823-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="4c823-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="4c823-113">To this state:</span></span>  <br/> |<span data-ttu-id="4c823-114">[Estado del mensaje de carga](upload-message-state.md), cargar estado de [eliminación](upload-delete-status-state.md), [cargar estado de lectura](upload-read-status-state.md)o sincronizar estado de contenido</span><span class="sxs-lookup"><span data-stu-id="4c823-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4c823-115">La máquina de estado de replicación es un equipo de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="4c823-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4c823-116">Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda.</span><span class="sxs-lookup"><span data-stu-id="4c823-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4c823-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c823-117">Description</span></span>

<span data-ttu-id="4c823-118">Este estado inicia la carga del contenido de una carpeta que se ha especificado en el estado de sincronizar contenido anterior.</span><span class="sxs-lookup"><span data-stu-id="4c823-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="4c823-119">La carpeta puede ser una carpeta de correo, calendario, contactos, tareas, notas o diario.</span><span class="sxs-lookup"><span data-stu-id="4c823-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="4c823-120">Durante este estado, Outlook crea una lista de elementos que se han agregado, modificado, movido, eliminado o marcado como leído y prepara la información interna adecuada para el estado de mensaje de carga correspondiente, carga el estado de eliminación de carga o carga estado de lectura. Estado.</span><span class="sxs-lookup"><span data-stu-id="4c823-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="4c823-121">Cuando finaliza este estado, Outlook marca la carpeta como que su contenido está sincronizado, por lo que el contenido no se cargará de nuevo hasta que se realice otra modificación.</span><span class="sxs-lookup"><span data-stu-id="4c823-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="4c823-122">El almacén local vuelve al estado Synchronize Contents.</span><span class="sxs-lookup"><span data-stu-id="4c823-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4c823-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="4c823-123">See also</span></span>



[<span data-ttu-id="4c823-124">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="4c823-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4c823-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="4c823-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4c823-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="4c823-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4c823-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="4c823-127">SYNCSTATE</span></span>](syncstate.md)

