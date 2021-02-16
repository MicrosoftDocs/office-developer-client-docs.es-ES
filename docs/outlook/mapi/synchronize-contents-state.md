---
title: Sincronizar el estado de contenido
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438473"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="41962-103">Sincronizar el estado de contenido</span><span class="sxs-lookup"><span data-stu-id="41962-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="41962-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41962-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="41962-105">En este tema se describe lo que sucede durante el estado del contenido de sincronización de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="41962-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="41962-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="41962-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41962-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="41962-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="41962-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="41962-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="41962-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="41962-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="41962-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="41962-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="41962-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="41962-111">From this state:</span></span>  <br/> |[<span data-ttu-id="41962-112">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="41962-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="41962-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="41962-113">To this state:</span></span>  <br/> |<span data-ttu-id="41962-114">[Descargar el estado de la tabla,](download-table-state.md) [cargar el estado de la](upload-table-state.md)tabla o sincronizar el estado</span><span class="sxs-lookup"><span data-stu-id="41962-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="41962-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="41962-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="41962-116">Un cliente que va de un estado a otro debe volver al primero desde el segundo.</span><span class="sxs-lookup"><span data-stu-id="41962-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="41962-117">Description</span><span class="sxs-lookup"><span data-stu-id="41962-117">Description</span></span>

<span data-ttu-id="41962-118">Este estado inicia uno de los dos procesos de replicación: cargar el contenido de las carpetas especificadas en un almacén local o una sincronización completa.</span><span class="sxs-lookup"><span data-stu-id="41962-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="41962-119">En una sincronización completa, para cada una de las carpetas especificadas, el contenido se carga primero y, a continuación, se descarga.</span><span class="sxs-lookup"><span data-stu-id="41962-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="41962-120">Según el  *ulFlags*  establecido en la estructura **[SYNC](sync.md)** correspondiente en el estado de sincronización anterior, Outlook inicializa los miembros [out] en la estructura **SYNCCONT** para proporcionar información sobre el contenido.</span><span class="sxs-lookup"><span data-stu-id="41962-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="41962-121">A través de **la misma estructura SYNCCONT,** el cliente obtiene el recuento de las carpetas que tienen contenido que se va a cargar o descargar.</span><span class="sxs-lookup"><span data-stu-id="41962-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="41962-122">El cliente recorrerá cada una de estas carpetas moviendo el almacén local al estado de la tabla de carga para cargar una carpeta o moviendo el almacén local al estado de la tabla de descarga para descargar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="41962-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="41962-123">Además, el cliente obtiene identificadores de entrada para las carpetas que requieren replicación.</span><span class="sxs-lookup"><span data-stu-id="41962-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="41962-124">Cuando finaliza este estado, Outlook limpia su información interna.</span><span class="sxs-lookup"><span data-stu-id="41962-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="41962-125">El almacén local vuelve al estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="41962-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="41962-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="41962-126">See also</span></span>



[<span data-ttu-id="41962-127">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="41962-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="41962-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="41962-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="41962-129">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="41962-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="41962-130">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="41962-130">SYNCSTATE</span></span>](syncstate.md)

