---
title: Estado de sincronización de contenidos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a2bdbeb39cce1e62569f364875c3828cdd530c63
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577250"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="9a106-103">Estado de sincronización de contenidos</span><span class="sxs-lookup"><span data-stu-id="9a106-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="9a106-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a106-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9a106-105">En este tema se describe qué ocurre durante el estado del contenido de sincronizar de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="9a106-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9a106-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9a106-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a106-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="9a106-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="9a106-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="9a106-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="9a106-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="9a106-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="9a106-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="9a106-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="9a106-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="9a106-111">From this state:</span></span>  <br/> |[<span data-ttu-id="9a106-112">Sincronizar estado</span><span class="sxs-lookup"><span data-stu-id="9a106-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="9a106-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="9a106-113">To this state:</span></span>  <br/> |<span data-ttu-id="9a106-114">[Estado de la tabla de descarga](download-table-state.md), [cargar el estado de la tabla](upload-table-state.md), o sincronizar estado</span><span class="sxs-lookup"><span data-stu-id="9a106-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="9a106-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="9a106-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="9a106-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="9a106-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="9a106-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a106-117">Description</span></span>

<span data-ttu-id="9a106-118">Este estado inicia uno de los dos procesos de replicación: carga el contenido de especificado las carpetas en un almacén local o una sincronización completa.</span><span class="sxs-lookup"><span data-stu-id="9a106-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="9a106-119">En una sincronización completa, para cada una de las carpetas especificadas, contenido se cargan en primer lugar y, a continuación, se descargan.</span><span class="sxs-lookup"><span data-stu-id="9a106-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="9a106-120">Según la *ulFlags* establecer en la estructura de **[sincronización](sync.md)** correspondiente en el anterior sincronizar estado, Outlook inicializa [out] (miembros de) en la estructura **SYNCCONT** para proporcionar información sobre el contenido.</span><span class="sxs-lookup"><span data-stu-id="9a106-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="9a106-121">A través de la misma estructura **SYNCCONT** , el cliente obtiene el recuento de las carpetas que tienen contenido que se carga o descarga.</span><span class="sxs-lookup"><span data-stu-id="9a106-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="9a106-122">El cliente recorre en bucle cada una de estas carpetas mover el almacén local en el estado de la tabla de cargar para cargar una carpeta, o mover el almacén local para el estado de la tabla de descarga para descargar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="9a106-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="9a106-123">Además, el cliente obtiene los identificadores de entrada para las carpetas que requieren replicación.</span><span class="sxs-lookup"><span data-stu-id="9a106-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="9a106-124">Cuando finaliza este estado, Outlook limpia su información interna.</span><span class="sxs-lookup"><span data-stu-id="9a106-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="9a106-125">Devuelve el almacén local en el estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="9a106-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a106-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9a106-126">See also</span></span>



[<span data-ttu-id="9a106-127">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="9a106-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9a106-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9a106-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9a106-129">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="9a106-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9a106-130">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="9a106-130">SYNCSTATE</span></span>](syncstate.md)

