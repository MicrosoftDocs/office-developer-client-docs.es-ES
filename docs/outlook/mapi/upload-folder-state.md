---
title: Cargar estado de la carpeta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348429"
---
# <a name="upload-folder-state"></a><span data-ttu-id="94821-103">Cargar estado de la carpeta</span><span class="sxs-lookup"><span data-stu-id="94821-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="94821-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94821-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="94821-105">En este tema se describe lo que ocurre durante el estado de la carpeta de carga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="94821-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="94821-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="94821-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94821-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="94821-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="94821-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="94821-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="94821-109">Estructura de datos relacionada:</span><span class="sxs-lookup"><span data-stu-id="94821-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="94821-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="94821-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="94821-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="94821-111">From this state:</span></span>  <br/> |[<span data-ttu-id="94821-112">Cargar estado de la jerarquía</span><span class="sxs-lookup"><span data-stu-id="94821-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="94821-113">A este estado:</span><span class="sxs-lookup"><span data-stu-id="94821-113">To this state:</span></span>  <br/> |<span data-ttu-id="94821-114">Cargar estado de la jerarquía</span><span class="sxs-lookup"><span data-stu-id="94821-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="94821-115">La máquina de estado de replicación es un equipo de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="94821-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="94821-116">Un cliente que deja de estar en un estado a otro debe volver eventualmente a la primera parte de la segunda.</span><span class="sxs-lookup"><span data-stu-id="94821-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="94821-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="94821-117">Description</span></span>

<span data-ttu-id="94821-118">Este estado inicia la carga de una carpeta en una jerarquía que se ha especificado en un estado de jerarquía de carga anterior.</span><span class="sxs-lookup"><span data-stu-id="94821-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="94821-119">Durante este estado, Outlook proporciona el objeto de carpeta (si no se ha eliminado) y las marcas que indican el estado de la carpeta (nueva, movida, modificada o eliminada) como parte de la estructura de datos de **UPFLD** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="94821-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="94821-120">A continuación, el cliente carga esta información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="94821-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="94821-121">Si la carga se realiza correctamente, el cliente establece *ulFlags* en **UPFLD** en **UPF_OK**.</span><span class="sxs-lookup"><span data-stu-id="94821-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="94821-122">A continuación, Outlook borra su información interna sobre la solicitud para cargar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="94821-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="94821-123">Cuando finaliza la carga de la carpeta, el almacén local vuelve al estado de carga de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="94821-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="94821-124">Basándose en la estructura **[UPHIER](uphier.md)** correspondiente al estado de la jerarquía de carga anterior, Outlook determina si se debe continuar con la carga de la siguiente carpeta y preparar el siguiente estado de la carpeta de carga.</span><span class="sxs-lookup"><span data-stu-id="94821-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="94821-125">Si el cliente solo necesita cargar una carpeta, el cliente puede iniciar la replicación mediante el [Estado Synchronize](synchronize-state.md) sin especificar el estado de carga de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="94821-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="94821-126">El cliente establece determinados miembros de **[Sync](sync.md)** ( *ulFlags* a **UPS_UPLOAD_ONLY** y **UPS_ONE_FOLDER** y *FEID* en el identificador de la carpeta) para decir a Outlook que solo se cargará una carpeta.</span><span class="sxs-lookup"><span data-stu-id="94821-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94821-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="94821-127">See also</span></span>



[<span data-ttu-id="94821-128">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="94821-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="94821-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="94821-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="94821-130">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="94821-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="94821-131">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="94821-131">SYNCSTATE</span></span>](syncstate.md)

