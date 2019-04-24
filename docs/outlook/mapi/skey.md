---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c417e6f4412bc40e8c2ebc056514eb96f60798f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282680"
---
# <a name="skey"></a><span data-ttu-id="f28c9-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="f28c9-103">SKEY</span></span>

  
  
<span data-ttu-id="f28c9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f28c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f28c9-105">Clave de origen de un elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="f28c9-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f28c9-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="f28c9-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="f28c9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f28c9-107">Members</span></span>

 <span data-ttu-id="f28c9-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="f28c9-108">_guid_</span></span>
  
> <span data-ttu-id="f28c9-109">GUID del servidor que crea el objeto.</span><span class="sxs-lookup"><span data-stu-id="f28c9-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f28c9-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="f28c9-110">See also</span></span>



[<span data-ttu-id="f28c9-111">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="f28c9-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="f28c9-112">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="f28c9-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="f28c9-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="f28c9-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="f28c9-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="f28c9-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="f28c9-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="f28c9-115">UPREADE</span></span>](upreade.md)

