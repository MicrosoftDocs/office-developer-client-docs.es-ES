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
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436808"
---
# <a name="updel"></a><span data-ttu-id="dc759-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="dc759-103">UPDEL</span></span>

  
  
<span data-ttu-id="dc759-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc759-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc759-105">Información sobre los elementos que se han eliminado en un almacén local.</span><span class="sxs-lookup"><span data-stu-id="dc759-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="dc759-106">Esta información se usa durante el estado [de eliminación de carga.](upload-delete-status-state.md)</span><span class="sxs-lookup"><span data-stu-id="dc759-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dc759-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="dc759-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="dc759-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc759-108">Members</span></span>

 <span data-ttu-id="dc759-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="dc759-109">_pupde_</span></span>
  
>  <span data-ttu-id="dc759-110">[salida] Vector de [entradas UPDELE.](updele.md)</span><span class="sxs-lookup"><span data-stu-id="dc759-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="dc759-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="dc759-111">_cEnt_</span></span>
  
> <span data-ttu-id="dc759-112">[salida] Número de entradas en *el archivo .*</span><span class="sxs-lookup"><span data-stu-id="dc759-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="dc759-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc759-113">See also</span></span>



[<span data-ttu-id="dc759-114">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="dc759-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="dc759-115">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="dc759-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="dc759-116">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="dc759-116">MAPI Constants</span></span>](mapi-constants.md)

