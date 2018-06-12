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
ms.openlocfilehash: bb2d347d218a7c33a2184bf1fcf181a11fa7d8fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816808"
---
# <a name="feid"></a><span data-ttu-id="5a2ce-103">FEID</span><span class="sxs-lookup"><span data-stu-id="5a2ce-103">FEID</span></span>

 
  
<span data-ttu-id="5a2ce-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a2ce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a2ce-105">Identificador de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="5a2ce-105">Identifier for a folder.</span></span> <span data-ttu-id="5a2ce-106">Contiene un identificador de entrada y otra información relevante.</span><span class="sxs-lookup"><span data-stu-id="5a2ce-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5a2ce-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="5a2ce-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="5a2ce-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a2ce-108">Members</span></span>

 <span data-ttu-id="5a2ce-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="5a2ce-109">_abFlags_</span></span>
  
> <span data-ttu-id="5a2ce-110">identificador de entrada de 4 bytes de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="5a2ce-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="5a2ce-111">Para obtener más información acerca de los identificadores de entrada MAPI, vea la **[propiedad ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="5a2ce-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="5a2ce-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="5a2ce-112">_muid_</span></span>
  
> <span data-ttu-id="5a2ce-113">GUID que identifica el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5a2ce-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="5a2ce-114">Vea mapidefs.h para la definición de tipo de **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="5a2ce-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="5a2ce-115">_marcador de posición_</span><span class="sxs-lookup"><span data-stu-id="5a2ce-115">_placeholder_</span></span>
  
> <span data-ttu-id="5a2ce-116">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="5a2ce-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="5a2ce-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="5a2ce-117">_ltid_</span></span>
  
> <span data-ttu-id="5a2ce-118">Identificador a largo plazo de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="5a2ce-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a2ce-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="5a2ce-119">See also</span></span>



[<span data-ttu-id="5a2ce-120">Acerca de la máquina de estado de replicación</span><span class="sxs-lookup"><span data-stu-id="5a2ce-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="5a2ce-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5a2ce-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5a2ce-122">LTID</span><span class="sxs-lookup"><span data-stu-id="5a2ce-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="5a2ce-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="5a2ce-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="5a2ce-124">SINCRONIZACIÓN</span><span class="sxs-lookup"><span data-stu-id="5a2ce-124">SYNC</span></span>](sync.md)

