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
ms.openlocfilehash: f4ece0662b72047b785b03f3134c96fac48c219a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820698"
---
# <a name="skey"></a><span data-ttu-id="dc685-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="dc685-103">SKEY</span></span>

  
  
<span data-ttu-id="dc685-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc685-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc685-105">Clave de origen para un elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="dc685-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dc685-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="dc685-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="dc685-107">Members</span><span class="sxs-lookup"><span data-stu-id="dc685-107">Members</span></span>

 <span data-ttu-id="dc685-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="dc685-108">_guid_</span></span>
  
> <span data-ttu-id="dc685-109">GUID de la creación del objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="dc685-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc685-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc685-110">See also</span></span>



[<span data-ttu-id="dc685-111">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="dc685-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="dc685-112">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="dc685-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="dc685-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="dc685-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="dc685-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="dc685-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="dc685-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="dc685-115">UPREADE</span></span>](upreade.md)

