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
# <a name="meid"></a><span data-ttu-id="27aaf-103">MEID</span><span class="sxs-lookup"><span data-stu-id="27aaf-103">MEID</span></span>

 
  
<span data-ttu-id="27aaf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27aaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27aaf-105">Identificador de un elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="27aaf-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="27aaf-106">Contiene un identificador de entrada y otra información relevante.</span><span class="sxs-lookup"><span data-stu-id="27aaf-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="27aaf-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="27aaf-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="27aaf-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="27aaf-108">Members</span></span>

 <span data-ttu-id="27aaf-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="27aaf-109">_abFlags_</span></span>
  
> <span data-ttu-id="27aaf-110">Identificador de entrada de 4 bytes para el elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="27aaf-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="27aaf-111">Para obtener más información acerca de los identificadores de entrada MAPI, **[vea ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="27aaf-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="27aaf-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="27aaf-112">_muid_</span></span>
  
> <span data-ttu-id="27aaf-113">GUID que identifica el proveedor de almacén.</span><span class="sxs-lookup"><span data-stu-id="27aaf-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="27aaf-114">Vea mapidefs.h para obtener la definición de tipo **de MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="27aaf-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="27aaf-115">_marcador de posición_</span><span class="sxs-lookup"><span data-stu-id="27aaf-115">_placeholder_</span></span>
  
> <span data-ttu-id="27aaf-116">Este miembro está reservado para el uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="27aaf-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="27aaf-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="27aaf-117">_ltidFld_</span></span>
  
> <span data-ttu-id="27aaf-118">Identificador a largo plazo de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="27aaf-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="27aaf-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="27aaf-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="27aaf-120">Identificador a largo plazo del elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="27aaf-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27aaf-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="27aaf-121">See also</span></span>



[<span data-ttu-id="27aaf-122">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="27aaf-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="27aaf-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="27aaf-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="27aaf-124">LTID</span><span class="sxs-lookup"><span data-stu-id="27aaf-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="27aaf-125">Sincronizar</span><span class="sxs-lookup"><span data-stu-id="27aaf-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="27aaf-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="27aaf-126">UPMSG</span></span>](upmsg.md)

