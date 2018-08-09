---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Última modificación: 03 de julio de 2012'
ms.openlocfilehash: 1b725dc5151f1f088f2547a1ef82d322c8458b6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818412"
---
# <a name="meid"></a><span data-ttu-id="079b0-103">MEID</span><span class="sxs-lookup"><span data-stu-id="079b0-103">MEID</span></span>

 
  
<span data-ttu-id="079b0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="079b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="079b0-105">Identificador de un elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="079b0-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="079b0-106">Contiene un identificador de entrada y otra información relevante.</span><span class="sxs-lookup"><span data-stu-id="079b0-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="079b0-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="079b0-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="079b0-108">Members</span><span class="sxs-lookup"><span data-stu-id="079b0-108">Members</span></span>

 <span data-ttu-id="079b0-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="079b0-109">_abFlags_</span></span>
  
> <span data-ttu-id="079b0-110">identificador de entrada de 4 bytes para el elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="079b0-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="079b0-111">Para obtener más información acerca de los identificadores de entrada MAPI, vea la **[propiedad ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="079b0-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="079b0-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="079b0-112">_muid_</span></span>
  
> <span data-ttu-id="079b0-113">GUID que identifica el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="079b0-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="079b0-114">Vea mapidefs.h para la definición de tipo de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="079b0-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="079b0-115">_marcador de posición_</span><span class="sxs-lookup"><span data-stu-id="079b0-115">_placeholder_</span></span>
  
> <span data-ttu-id="079b0-116">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="079b0-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="079b0-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="079b0-117">_ltidFld_</span></span>
  
> <span data-ttu-id="079b0-118">Identificador a largo plazo de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="079b0-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="079b0-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="079b0-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="079b0-120">Identificador a largo plazo del elemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="079b0-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="079b0-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="079b0-121">See also</span></span>



[<span data-ttu-id="079b0-122">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="079b0-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="079b0-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="079b0-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="079b0-124">LTID</span><span class="sxs-lookup"><span data-stu-id="079b0-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="079b0-125">SYNC</span><span class="sxs-lookup"><span data-stu-id="079b0-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="079b0-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="079b0-126">UPMSG</span></span>](upmsg.md)

