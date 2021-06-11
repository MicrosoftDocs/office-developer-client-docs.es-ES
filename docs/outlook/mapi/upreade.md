---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434147"
---
# <a name="upreade"></a><span data-ttu-id="26370-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="26370-103">UPREADE</span></span>

<span data-ttu-id="26370-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26370-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26370-105">Información extendida para cargar el estado de lectura de un elemento durante el [estado de lectura de carga.](upload-read-status-state.md)</span><span class="sxs-lookup"><span data-stu-id="26370-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="26370-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="26370-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="26370-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="26370-107">Members</span></span>

<span data-ttu-id="26370-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="26370-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="26370-109">[out]/[in] Marca para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="26370-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="26370-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="26370-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="26370-111">[salida] El elemento está oculto.</span><span class="sxs-lookup"><span data-stu-id="26370-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="26370-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="26370-112">UPR_READ</span></span>
    
    - <span data-ttu-id="26370-113">[salida] Se ha cambiado el estado de lectura del elemento.</span><span class="sxs-lookup"><span data-stu-id="26370-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="26370-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="26370-114">UPR_OK</span></span>
    
    - <span data-ttu-id="26370-115">[in] Upload se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="26370-115">[in] Upload was successful.</span></span> <span data-ttu-id="26370-116">El cliente lo establece después de cargar información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="26370-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="26370-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="26370-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="26370-118">[in] Upload estado de lectura del elemento ahora, en lugar de esperar al final del estado de la tabla [de](upload-table-state.md) carga para procesar por lotes más de un elemento.</span><span class="sxs-lookup"><span data-stu-id="26370-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="26370-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="26370-119">_skey_</span></span>
  
> <span data-ttu-id="26370-120">[salida] Clave de origen del elemento.</span><span class="sxs-lookup"><span data-stu-id="26370-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26370-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="26370-121">See also</span></span>

- [<span data-ttu-id="26370-122">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="26370-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="26370-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="26370-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="26370-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="26370-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="26370-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="26370-125">UPREAD</span></span>](upread.md)

