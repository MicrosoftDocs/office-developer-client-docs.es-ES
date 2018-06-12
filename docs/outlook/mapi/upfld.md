---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: f25b3fb967f4ed93ac38487f21145f35413764da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820930"
---
# <a name="upfld"></a><span data-ttu-id="77517-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="77517-103">UPFLD</span></span>

<span data-ttu-id="77517-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77517-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="77517-105">Información para cargar una carpeta durante la [carga de estado de la carpeta](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="77517-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="77517-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="77517-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="77517-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="77517-107">Members</span></span>

<span data-ttu-id="77517-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="77517-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="77517-109">[out] / [in] indicadores para determinar las acciones adecuadas para el uplaod.</span><span class="sxs-lookup"><span data-stu-id="77517-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="77517-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="77517-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="77517-111">[out] Carpeta es nueva.</span><span class="sxs-lookup"><span data-stu-id="77517-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="77517-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="77517-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="77517-113">[out] Se ha movido la carpeta.</span><span class="sxs-lookup"><span data-stu-id="77517-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="77517-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="77517-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="77517-115">[out] Propiedades de la carpeta se han modificado.</span><span class="sxs-lookup"><span data-stu-id="77517-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="77517-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="77517-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="77517-117">[out] Se eliminó la carpeta.</span><span class="sxs-lookup"><span data-stu-id="77517-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="77517-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="77517-118">UPF_OK</span></span>
    
    - <span data-ttu-id="77517-119">[entrada] Carga fue correcta.</span><span class="sxs-lookup"><span data-stu-id="77517-119">[in] Upload was successful.</span></span> <span data-ttu-id="77517-120">El cliente establece esto después de cargar la información de la carpeta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="77517-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="77517-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="77517-121">_pfld_</span></span>
  
> <span data-ttu-id="77517-122">[out] El objeto de carpeta abierta para cargar.</span><span class="sxs-lookup"><span data-stu-id="77517-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="77517-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="77517-123">_feid_</span></span>
  
> <span data-ttu-id="77517-124">[out] Identificador de entrada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="77517-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77517-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="77517-125">See also</span></span>

- [<span data-ttu-id="77517-126">Acerca de la API de replicación</span><span class="sxs-lookup"><span data-stu-id="77517-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="77517-127">Acerca de la máquina de estado de replicación</span><span class="sxs-lookup"><span data-stu-id="77517-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="77517-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="77517-128">MAPI Constants</span></span>](mapi-constants.md)

