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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426810"
---
# <a name="skey"></a><span data-ttu-id="5b3f2-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="5b3f2-103">SKEY</span></span>

  
  
<span data-ttu-id="5b3f2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b3f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b3f2-105">Clave de origen de un elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="5b3f2-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5b3f2-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="5b3f2-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="5b3f2-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5b3f2-107">Members</span></span>

 <span data-ttu-id="5b3f2-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="5b3f2-108">_guid_</span></span>
  
> <span data-ttu-id="5b3f2-109">GUID del servidor que crea el objeto.</span><span class="sxs-lookup"><span data-stu-id="5b3f2-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b3f2-110">Ver también</span><span class="sxs-lookup"><span data-stu-id="5b3f2-110">See also</span></span>



[<span data-ttu-id="5b3f2-111">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="5b3f2-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="5b3f2-112">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="5b3f2-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="5b3f2-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="5b3f2-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="5b3f2-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="5b3f2-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="5b3f2-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="5b3f2-115">UPREADE</span></span>](upreade.md)

