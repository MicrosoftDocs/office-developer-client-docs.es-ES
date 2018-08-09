---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bfc03f7fe573005a235154cf179dcf44bf4abd65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820925"
---
# <a name="updel"></a><span data-ttu-id="3c97d-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="3c97d-103">UPDEL</span></span>

  
  
<span data-ttu-id="3c97d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3c97d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3c97d-105">Información para los elementos que se han eliminado en un almacén local.</span><span class="sxs-lookup"><span data-stu-id="3c97d-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="3c97d-106">Esta información se usa durante la [carga Eliminar estado](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="3c97d-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3c97d-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="3c97d-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="3c97d-108">Members</span><span class="sxs-lookup"><span data-stu-id="3c97d-108">Members</span></span>

 <span data-ttu-id="3c97d-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="3c97d-109">_pupde_</span></span>
  
>  <span data-ttu-id="3c97d-110">[out] Vector de [UPDELE](updele.md) entradas.</span><span class="sxs-lookup"><span data-stu-id="3c97d-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="3c97d-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="3c97d-111">_cEnt_</span></span>
  
> <span data-ttu-id="3c97d-112">[out] Número de entradas en *pupde* .</span><span class="sxs-lookup"><span data-stu-id="3c97d-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3c97d-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c97d-113">See also</span></span>



[<span data-ttu-id="3c97d-114">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="3c97d-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3c97d-115">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="3c97d-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3c97d-116">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3c97d-116">MAPI Constants</span></span>](mapi-constants.md)

