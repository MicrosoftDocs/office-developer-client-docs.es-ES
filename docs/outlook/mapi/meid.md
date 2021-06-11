---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430311"
---
# <a name="meid"></a><span data-ttu-id="2e8fd-103">MEID</span><span class="sxs-lookup"><span data-stu-id="2e8fd-103">MEID</span></span>

 
  
<span data-ttu-id="2e8fd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e8fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e8fd-105">Identificador de un Outlook elemento.</span><span class="sxs-lookup"><span data-stu-id="2e8fd-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="2e8fd-106">Contiene un identificador de entrada y otra información relevante.</span><span class="sxs-lookup"><span data-stu-id="2e8fd-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2e8fd-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="2e8fd-107">Quick info</span></span>

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a><span data-ttu-id="2e8fd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e8fd-108">Members</span></span>

 <span data-ttu-id="2e8fd-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="2e8fd-109">_abFlags_</span></span>
  
> <span data-ttu-id="2e8fd-110">Identificador de entrada de 4 bytes para el Outlook elemento.</span><span class="sxs-lookup"><span data-stu-id="2e8fd-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="2e8fd-111">Para obtener más información acerca de los identificadores de entrada MAPI, vea **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="2e8fd-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="2e8fd-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="2e8fd-112">_muid_</span></span>
  
> <span data-ttu-id="2e8fd-113">GUID que identifica el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2e8fd-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="2e8fd-114">Vea mapidefs.h para obtener la definición de tipo **de MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="2e8fd-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="2e8fd-115">_marcador de posición_</span><span class="sxs-lookup"><span data-stu-id="2e8fd-115">_placeholder_</span></span>
  
> <span data-ttu-id="2e8fd-116">Este miembro está reservado para el uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="2e8fd-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="2e8fd-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="2e8fd-117">_ltidFld_</span></span>
  
> <span data-ttu-id="2e8fd-118">Identificador a largo plazo de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2e8fd-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="2e8fd-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="2e8fd-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="2e8fd-120">Identificador a largo plazo del Outlook elemento.</span><span class="sxs-lookup"><span data-stu-id="2e8fd-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e8fd-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e8fd-121">See also</span></span>



[<span data-ttu-id="2e8fd-122">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="2e8fd-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2e8fd-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="2e8fd-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2e8fd-124">LTID</span><span class="sxs-lookup"><span data-stu-id="2e8fd-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="2e8fd-125">Sincronizar</span><span class="sxs-lookup"><span data-stu-id="2e8fd-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="2e8fd-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="2e8fd-126">UPMSG</span></span>](upmsg.md)

