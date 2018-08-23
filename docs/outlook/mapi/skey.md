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
ms.openlocfilehash: 26b08535d81cb961ed0ace70ea227316b30cd526
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573463"
---
# <a name="skey"></a><span data-ttu-id="2af5e-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="2af5e-103">SKEY</span></span>

  
  
<span data-ttu-id="2af5e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2af5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2af5e-105">Clave de origen para un elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="2af5e-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2af5e-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="2af5e-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="2af5e-107">Members</span><span class="sxs-lookup"><span data-stu-id="2af5e-107">Members</span></span>

 <span data-ttu-id="2af5e-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="2af5e-108">_guid_</span></span>
  
> <span data-ttu-id="2af5e-109">GUID de la creación del objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="2af5e-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2af5e-110">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2af5e-110">See also</span></span>



[<span data-ttu-id="2af5e-111">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="2af5e-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2af5e-112">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="2af5e-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2af5e-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="2af5e-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="2af5e-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="2af5e-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="2af5e-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="2af5e-115">UPREADE</span></span>](upreade.md)

