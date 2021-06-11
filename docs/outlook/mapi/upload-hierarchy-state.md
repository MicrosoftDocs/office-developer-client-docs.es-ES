---
title: Upload Estado de jerarquía
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415428"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="8e8c7-103">Upload Estado de jerarquía</span><span class="sxs-lookup"><span data-stu-id="8e8c7-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="8e8c7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e8c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8e8c7-105">En este tema se describe lo que sucede durante el estado de la jerarquía de carga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="8e8c7-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8e8c7-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="8e8c7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e8c7-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="8e8c7-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="8e8c7-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="8e8c7-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="8e8c7-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="8e8c7-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="8e8c7-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="8e8c7-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="8e8c7-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="8e8c7-111">From this state:</span></span>  <br/> |[<span data-ttu-id="8e8c7-112">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="8e8c7-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="8e8c7-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="8e8c7-113">To this state:</span></span>  <br/> |<span data-ttu-id="8e8c7-114">[Upload de carpeta o](upload-folder-state.md)sincronizar el estado</span><span class="sxs-lookup"><span data-stu-id="8e8c7-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="8e8c7-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="8e8c7-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="8e8c7-116">Un cliente que se va de un estado a otro debe volver finalmente al primero desde el segundo.</span><span class="sxs-lookup"><span data-stu-id="8e8c7-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="8e8c7-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e8c7-117">Description</span></span>

<span data-ttu-id="8e8c7-118">Este estado inicia la carga de una jerarquía de árbol de carpetas que se ha especificado en un estado de sincronización anterior.</span><span class="sxs-lookup"><span data-stu-id="8e8c7-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="8e8c7-119">Outlook determina el número de carpetas que se han creado o modificado en esa jerarquía e inicializa *cEnt* en **UPHIER**.</span><span class="sxs-lookup"><span data-stu-id="8e8c7-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="8e8c7-120">Outlook también mantiene un recuento del número de carpetas cargadas con otro *miembro iEnt* .</span><span class="sxs-lookup"><span data-stu-id="8e8c7-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="8e8c7-121">Para cargar cada una de las carpetas  *de cEnt,*  el cliente mueve el almacén local al estado de la carpeta de carga, volviendo al estado de jerarquía de carga cuando finaliza la carga de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="8e8c7-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="8e8c7-122">Cuando finaliza el estado de la jerarquía de carga, el almacén local vuelve al estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="8e8c7-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e8c7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e8c7-123">See also</span></span>



[<span data-ttu-id="8e8c7-124">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="8e8c7-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="8e8c7-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="8e8c7-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8e8c7-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="8e8c7-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="8e8c7-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="8e8c7-127">SYNCSTATE</span></span>](syncstate.md)

