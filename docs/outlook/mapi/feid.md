---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Última modificación: 02 de julio de 2012'
ms.openlocfilehash: 3e534f91863e2a1300e03d112d1f532f486eedd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588310"
---
# <a name="feid"></a><span data-ttu-id="e4253-103">FEID</span><span class="sxs-lookup"><span data-stu-id="e4253-103">FEID</span></span>

 
  
<span data-ttu-id="e4253-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4253-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4253-105">Identificador de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="e4253-105">Identifier for a folder.</span></span> <span data-ttu-id="e4253-106">Contiene un identificador de entrada y otra información relevante.</span><span class="sxs-lookup"><span data-stu-id="e4253-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e4253-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e4253-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="e4253-108">Members</span><span class="sxs-lookup"><span data-stu-id="e4253-108">Members</span></span>

 <span data-ttu-id="e4253-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="e4253-109">_abFlags_</span></span>
  
> <span data-ttu-id="e4253-110">identificador de entrada de 4 bytes de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e4253-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="e4253-111">Para obtener más información acerca de los identificadores de entrada MAPI, vea la **[propiedad ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="e4253-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="e4253-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="e4253-112">_muid_</span></span>
  
> <span data-ttu-id="e4253-113">GUID que identifica el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="e4253-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="e4253-114">Vea mapidefs.h para la definición de tipo de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="e4253-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="e4253-115">_marcador de posición_</span><span class="sxs-lookup"><span data-stu-id="e4253-115">_placeholder_</span></span>
  
> <span data-ttu-id="e4253-116">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="e4253-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="e4253-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="e4253-117">_ltid_</span></span>
  
> <span data-ttu-id="e4253-118">Identificador a largo plazo de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e4253-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4253-119">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e4253-119">See also</span></span>



[<span data-ttu-id="e4253-120">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="e4253-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e4253-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e4253-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e4253-122">LTID</span><span class="sxs-lookup"><span data-stu-id="e4253-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="e4253-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="e4253-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="e4253-124">SYNC</span><span class="sxs-lookup"><span data-stu-id="e4253-124">SYNC</span></span>](sync.md)

