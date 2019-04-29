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
# <a name="upreade"></a><span data-ttu-id="36fdb-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="36fdb-103">UPREADE</span></span>

<span data-ttu-id="36fdb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36fdb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36fdb-105">Información extendida para cargar el estado de lectura de un elemento durante el [Estado de lectura](upload-read-status-state.md)de la carga.</span><span class="sxs-lookup"><span data-stu-id="36fdb-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="36fdb-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="36fdb-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="36fdb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="36fdb-107">Members</span></span>

<span data-ttu-id="36fdb-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36fdb-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="36fdb-109">[salida]/[in] indicadores para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="36fdb-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="36fdb-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="36fdb-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="36fdb-111">contempla El elemento está oculto.</span><span class="sxs-lookup"><span data-stu-id="36fdb-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="36fdb-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="36fdb-112">UPR_READ</span></span>
    
    - <span data-ttu-id="36fdb-113">contempla Se ha cambiado el estado de lectura del elemento.</span><span class="sxs-lookup"><span data-stu-id="36fdb-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="36fdb-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="36fdb-114">UPR_OK</span></span>
    
    - <span data-ttu-id="36fdb-115">a La carga se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="36fdb-115">[in] Upload was successful.</span></span> <span data-ttu-id="36fdb-116">El cliente lo establece después de cargar la información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="36fdb-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="36fdb-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="36fdb-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="36fdb-118">a Cargue ahora el estado de lectura del elemento, en lugar de esperar hasta el final del [Estado de carga](upload-table-state.md) de la tabla, para procesar por lotes más de un elemento.</span><span class="sxs-lookup"><span data-stu-id="36fdb-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="36fdb-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="36fdb-119">_skey_</span></span>
  
> <span data-ttu-id="36fdb-120">contempla Clave de origen del elemento.</span><span class="sxs-lookup"><span data-stu-id="36fdb-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36fdb-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="36fdb-121">See also</span></span>

- [<span data-ttu-id="36fdb-122">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="36fdb-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="36fdb-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="36fdb-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="36fdb-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="36fdb-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="36fdb-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="36fdb-125">UPREAD</span></span>](upread.md)

