---
title: Upload Estado de tabla
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
# <a name="upload-table-state"></a><span data-ttu-id="a670c-103">Upload Estado de tabla</span><span class="sxs-lookup"><span data-stu-id="a670c-103">Upload Table State</span></span>

  
  
<span data-ttu-id="a670c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a670c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a670c-105">En este tema se describe lo que sucede durante el estado de la tabla de carga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="a670c-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a670c-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="a670c-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a670c-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="a670c-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="a670c-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="a670c-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="a670c-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="a670c-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="a670c-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="a670c-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="a670c-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="a670c-111">From this state:</span></span>  <br/> |[<span data-ttu-id="a670c-112">Sincronizar el estado de contenido</span><span class="sxs-lookup"><span data-stu-id="a670c-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="a670c-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="a670c-113">To this state:</span></span>  <br/> |<span data-ttu-id="a670c-114">[Upload de mensaje,](upload-message-state.md)estado de [eliminación de carga,](upload-delete-status-state.md)estado de lectura [de](upload-read-status-state.md)carga o estado de sincronización de contenido</span><span class="sxs-lookup"><span data-stu-id="a670c-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a670c-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="a670c-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="a670c-116">Un cliente que sale de un estado a otro debe volver al primero desde el segundo.</span><span class="sxs-lookup"><span data-stu-id="a670c-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="a670c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a670c-117">Description</span></span>

<span data-ttu-id="a670c-118">Este estado inicia la carga del contenido de una carpeta que se ha especificado en un estado de contenido de sincronización anterior.</span><span class="sxs-lookup"><span data-stu-id="a670c-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="a670c-119">La carpeta puede ser una carpeta de correo, calendario, contactos, tareas, notas o diario.</span><span class="sxs-lookup"><span data-stu-id="a670c-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="a670c-120">Durante este estado, Outlook crea una lista de elementos que se han agregado, modificado, movido, eliminado o marcado como leído, y prepara la información interna adecuada para el estado del mensaje de carga correspondiente, el estado de la eliminación de carga o el estado de lectura de carga.</span><span class="sxs-lookup"><span data-stu-id="a670c-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="a670c-121">Cuando finalice este estado, Outlook marca la carpeta como que su contenido esté sincronizado, de modo que el contenido no se vuelva a cargar hasta que se haga otra modificación.</span><span class="sxs-lookup"><span data-stu-id="a670c-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="a670c-122">El almacén local vuelve al estado de sincronización de contenido.</span><span class="sxs-lookup"><span data-stu-id="a670c-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a670c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a670c-123">See also</span></span>



[<span data-ttu-id="a670c-124">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="a670c-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a670c-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a670c-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a670c-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="a670c-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a670c-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a670c-127">SYNCSTATE</span></span>](syncstate.md)

