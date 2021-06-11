---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431361"
---
# <a name="upfld"></a><span data-ttu-id="91508-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="91508-103">UPFLD</span></span>

<span data-ttu-id="91508-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91508-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91508-105">Información para cargar una carpeta durante el [estado de la carpeta de carga.](upload-folder-state.md)</span><span class="sxs-lookup"><span data-stu-id="91508-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="91508-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="91508-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="91508-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="91508-107">Members</span></span>

<span data-ttu-id="91508-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="91508-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="91508-109">[out]/[in] Marca para determinar las acciones adecuadas para el uplaod.</span><span class="sxs-lookup"><span data-stu-id="91508-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="91508-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="91508-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="91508-111">[salida] La carpeta es nueva.</span><span class="sxs-lookup"><span data-stu-id="91508-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="91508-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="91508-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="91508-113">[salida] Se ha movido la carpeta.</span><span class="sxs-lookup"><span data-stu-id="91508-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="91508-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="91508-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="91508-115">[salida] Se han modificado las propiedades de carpeta.</span><span class="sxs-lookup"><span data-stu-id="91508-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="91508-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="91508-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="91508-117">[salida] Se eliminó la carpeta.</span><span class="sxs-lookup"><span data-stu-id="91508-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="91508-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="91508-118">UPF_OK</span></span>
    
    - <span data-ttu-id="91508-119">[in] Upload se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="91508-119">[in] Upload was successful.</span></span> <span data-ttu-id="91508-120">El cliente establece esto después de cargar información de carpeta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="91508-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="91508-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="91508-121">_pfld_</span></span>
  
> <span data-ttu-id="91508-122">[salida] Objeto de carpeta abierta que se cargará.</span><span class="sxs-lookup"><span data-stu-id="91508-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="91508-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="91508-123">_feid_</span></span>
  
> <span data-ttu-id="91508-124">[salida] Id. de entrada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="91508-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91508-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="91508-125">See also</span></span>

- [<span data-ttu-id="91508-126">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="91508-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="91508-127">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="91508-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="91508-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="91508-128">MAPI Constants</span></span>](mapi-constants.md)

