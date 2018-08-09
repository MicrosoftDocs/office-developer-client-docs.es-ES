---
title: Cargar estado de la carpeta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 82b00a33c5de11b3fc9ccd3bde4cf31c79b99c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820928"
---
# <a name="upload-folder-state"></a><span data-ttu-id="b2a2e-103">Cargar estado de la carpeta</span><span class="sxs-lookup"><span data-stu-id="b2a2e-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="b2a2e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2a2e-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="b2a2e-105">En este tema se describe qué ocurre durante el estado de la carpeta de carga de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b2a2e-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="b2a2e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2a2e-107">Identificador de estado:</span><span class="sxs-lookup"><span data-stu-id="b2a2e-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="b2a2e-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="b2a2e-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="b2a2e-109">Estructura de datos relacionados:</span><span class="sxs-lookup"><span data-stu-id="b2a2e-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="b2a2e-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="b2a2e-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="b2a2e-111">Desde este estado:</span><span class="sxs-lookup"><span data-stu-id="b2a2e-111">From this state:</span></span>  <br/> |[<span data-ttu-id="b2a2e-112">Cargar el estado de la jerarquía</span><span class="sxs-lookup"><span data-stu-id="b2a2e-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="b2a2e-113">En este estado:</span><span class="sxs-lookup"><span data-stu-id="b2a2e-113">To this state:</span></span>  <br/> |<span data-ttu-id="b2a2e-114">Cargar el estado de la jerarquía</span><span class="sxs-lookup"><span data-stu-id="b2a2e-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b2a2e-115">La máquina de estado de replicación es una máquina de estado determinista.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="b2a2e-116">Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="b2a2e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2a2e-117">Description</span></span>

<span data-ttu-id="b2a2e-118">Este estado inicia la carga de una carpeta en una jerarquía que se haya especificado en un estado de jerarquía anterior de carga.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="b2a2e-119">Durante este estado, Outlook proporciona el objeto de carpeta (si no se ha eliminado) y los indicadores que indica el estado de la carpeta (nuevo, mover, modificar o eliminar) como parte de la estructura de datos **UPFLD** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="b2a2e-120">El cliente, a continuación, carga esta información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="b2a2e-121">Si la carga se realiza correctamente, el cliente establece *ulFlags* en **UPFLD** a **UPF_OK**.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="b2a2e-122">Outlook, a continuación, borra su información interna acerca de la solicitud para cargar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="b2a2e-123">Cuando finaliza la carga de la carpeta, el almacén local se devuelve en el estado de la jerarquía de carga.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="b2a2e-124">En función de la estructura **[UPHIER](uphier.md)** corresponde al estado de jerarquía anterior de carga, Outlook determina si para continuar con la carga de la carpeta siguiente y preparar para el estado de la carpeta de carga siguiente.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b2a2e-125">Si el cliente necesita cargar sólo una carpeta, el cliente puede iniciar la replicación a través de la [sincronización de estado](synchronize-state.md) sin tener que especificar el estado de la jerarquía de carga.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="b2a2e-126">El cliente establece ciertos miembros de **[sincronización](sync.md)** : *ulFlags* para **UPS_UPLOAD_ONLY** y **UPS_ONE_FOLDER** y *feid* para el identificador de la carpeta indicar a Outlook que sólo una carpeta se cargará.</span><span class="sxs-lookup"><span data-stu-id="b2a2e-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2a2e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2a2e-127">See also</span></span>



[<span data-ttu-id="b2a2e-128">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="b2a2e-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b2a2e-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b2a2e-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="b2a2e-130">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="b2a2e-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b2a2e-131">ESTADO DE SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="b2a2e-131">SYNCSTATE</span></span>](syncstate.md)

