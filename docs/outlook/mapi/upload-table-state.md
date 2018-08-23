---
title: Cargar estado de la tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bd54c30e8701a13637235e28ddcfef4c21d10a2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576984"
---
# <a name="upload-table-state"></a><span data-ttu-id="3bfe1-103">Cargar estado de la tabla</span><span class="sxs-lookup"><span data-stu-id="3bfe1-103">Upload Table State</span></span>

  
  
<span data-ttu-id="3bfe1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bfe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3bfe1-105">En este tema se describe qué ocurre durante el estado de la tabla de carga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="3bfe1-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3bfe1-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="3bfe1-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bfe1-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="3bfe1-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="3bfe1-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="3bfe1-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="3bfe1-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="3bfe1-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="3bfe1-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="3bfe1-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="3bfe1-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="3bfe1-111">From this state:</span></span>  <br/> |[<span data-ttu-id="3bfe1-112">Sincronizar el estado del contenido</span><span class="sxs-lookup"><span data-stu-id="3bfe1-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="3bfe1-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="3bfe1-113">To this state:</span></span>  <br/> |<span data-ttu-id="3bfe1-114">[Cargar el estado del mensaje](upload-message-state.md), [estado de estado de eliminación de carga](upload-delete-status-state.md), [leer el estado del estado de carga](upload-read-status-state.md), o sincronizar el estado del contenido</span><span class="sxs-lookup"><span data-stu-id="3bfe1-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3bfe1-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="3bfe1-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="3bfe1-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="3bfe1-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="3bfe1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bfe1-117">Description</span></span>

<span data-ttu-id="3bfe1-118">Este estado inicia carga el contenido de una carpeta que se haya especificado en un estado de contenido de sincronizar anterior.</span><span class="sxs-lookup"><span data-stu-id="3bfe1-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="3bfe1-119">La carpeta puede ser una carpeta de correo, calendario, contactos, tareas, notas o diario.</span><span class="sxs-lookup"><span data-stu-id="3bfe1-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="3bfe1-120">Durante este estado, Outlook crea una lista de elementos que se han agregado, modificado, movido, eliminado o marcado como leído y prepara la información interna adecuada para el estado del mensaje carga correspondiente, cargar el estado de eliminar o cargar el estado de lectura estado.</span><span class="sxs-lookup"><span data-stu-id="3bfe1-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="3bfe1-121">Cuando finaliza este estado, Outlook marca la carpeta como tener su contenido sincronizado, por lo que el contenido no se cargará nuevo hasta que se realiza otra modificación.</span><span class="sxs-lookup"><span data-stu-id="3bfe1-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="3bfe1-122">Devuelve el almacén local en el estado del contenido de sincronizar.</span><span class="sxs-lookup"><span data-stu-id="3bfe1-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3bfe1-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3bfe1-123">See also</span></span>



[<span data-ttu-id="3bfe1-124">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="3bfe1-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3bfe1-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3bfe1-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3bfe1-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="3bfe1-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3bfe1-127">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="3bfe1-127">SYNCSTATE</span></span>](syncstate.md)

