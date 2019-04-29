---
title: Cargar estado de la jerarquía
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
# <a name="upload-hierarchy-state"></a><span data-ttu-id="62da4-103">Cargar estado de la jerarquía</span><span class="sxs-lookup"><span data-stu-id="62da4-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="62da4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62da4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="62da4-105">En este tema se describe lo que ocurre durante el estado de la jerarquía de carga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="62da4-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="62da4-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="62da4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62da4-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="62da4-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="62da4-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="62da4-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="62da4-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="62da4-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="62da4-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="62da4-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="62da4-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="62da4-111">From this state:</span></span>  <br/> |[<span data-ttu-id="62da4-112">Estado de sincronización</span><span class="sxs-lookup"><span data-stu-id="62da4-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="62da4-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="62da4-113">To this state:</span></span>  <br/> |<span data-ttu-id="62da4-114">[Cargar el estado](upload-folder-state.md)de la carpeta o sincronizar el estado</span><span class="sxs-lookup"><span data-stu-id="62da4-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="62da4-115">La máquina de estado de replicación es un equipo de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="62da4-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="62da4-116">Un cliente que deja un estado a otro debe volver eventualmente a la primera parte de la segunda.</span><span class="sxs-lookup"><span data-stu-id="62da4-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="62da4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="62da4-117">Description</span></span>

<span data-ttu-id="62da4-118">Este estado inicia la carga de una jerarquía de árbol de carpetas que se ha especificado en un estado de sincronización anterior.</span><span class="sxs-lookup"><span data-stu-id="62da4-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="62da4-119">Outlook determina el número de carpetas que se han creado o modificado en esa jerarquía e inicializa *cEnt* en **UPHIER**.</span><span class="sxs-lookup"><span data-stu-id="62da4-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="62da4-120">Outlook también mantiene un recuento del número de carpetas cargadas con otro miembro *iEnt* .</span><span class="sxs-lookup"><span data-stu-id="62da4-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="62da4-121">Para cargar cada una de \*\* las carpetas de céntimos, el cliente mueve el almacén local al estado de carga de la carpeta, volviendo al estado de la jerarquía de carga cuando finaliza la carga de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="62da4-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="62da4-122">Cuando finaliza el estado de carga de la jerarquía, el almacén local vuelve al estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="62da4-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="62da4-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="62da4-123">See also</span></span>



[<span data-ttu-id="62da4-124">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="62da4-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="62da4-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="62da4-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="62da4-126">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="62da4-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="62da4-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="62da4-127">SYNCSTATE</span></span>](syncstate.md)

