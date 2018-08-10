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
ms.openlocfilehash: 854e674002953c31c47d56096700dca582ce0a5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820950"
---
# <a name="upreade"></a><span data-ttu-id="95398-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="95398-103">UPREADE</span></span>

<span data-ttu-id="95398-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95398-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95398-105">Información ampliada para cargar el estado de un elemento durante la [carga lee el estado de estado](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="95398-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="95398-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="95398-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="95398-107">Members</span><span class="sxs-lookup"><span data-stu-id="95398-107">Members</span></span>

<span data-ttu-id="95398-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="95398-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="95398-109">[out] o [in] indicadores para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="95398-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="95398-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="95398-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="95398-111">[out] Elemento está oculto.</span><span class="sxs-lookup"><span data-stu-id="95398-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="95398-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="95398-112">UPR_READ</span></span>
    
    - <span data-ttu-id="95398-113">[out] Se cambió el estado de lectura del elemento.</span><span class="sxs-lookup"><span data-stu-id="95398-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="95398-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="95398-114">UPR_OK</span></span>
    
    - <span data-ttu-id="95398-115">[entrada] Carga fue correcta.</span><span class="sxs-lookup"><span data-stu-id="95398-115">[in] Upload was successful.</span></span> <span data-ttu-id="95398-116">El cliente establece esto después de cargar información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="95398-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="95398-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="95398-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="95398-118">[entrada] Cargar el estado de lectura del elemento ahora, en lugar de esperar hasta el final de la [carga de estado de la tabla](upload-table-state.md) a proceso por lotes más de un elemento.</span><span class="sxs-lookup"><span data-stu-id="95398-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="95398-119">_SKEY_</span><span class="sxs-lookup"><span data-stu-id="95398-119">_skey_</span></span>
  
> <span data-ttu-id="95398-120">[out] Clave de origen del elemento.</span><span class="sxs-lookup"><span data-stu-id="95398-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95398-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="95398-121">See also</span></span>

- [<span data-ttu-id="95398-122">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="95398-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="95398-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="95398-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="95398-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="95398-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="95398-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="95398-125">UPREAD</span></span>](upread.md)
