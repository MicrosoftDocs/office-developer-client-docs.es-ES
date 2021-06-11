---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409814"
---
# <a name="feid"></a><span data-ttu-id="a7ad3-103">FEID</span><span class="sxs-lookup"><span data-stu-id="a7ad3-103">FEID</span></span>

 
  
<span data-ttu-id="a7ad3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7ad3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7ad3-105">Identificador de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a7ad3-105">Identifier for a folder.</span></span> <span data-ttu-id="a7ad3-106">Contiene un identificador de entrada y otra información relevante.</span><span class="sxs-lookup"><span data-stu-id="a7ad3-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a7ad3-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="a7ad3-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="a7ad3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a7ad3-108">Members</span></span>

 <span data-ttu-id="a7ad3-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="a7ad3-109">_abFlags_</span></span>
  
> <span data-ttu-id="a7ad3-110">Identificador de entrada de 4 bytes para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a7ad3-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="a7ad3-111">Para obtener más información acerca de los identificadores de entrada MAPI, vea **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="a7ad3-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="a7ad3-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="a7ad3-112">_muid_</span></span>
  
> <span data-ttu-id="a7ad3-113">GUID que identifica el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a7ad3-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="a7ad3-114">Vea mapidefs.h para obtener la definición de tipo **de MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="a7ad3-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="a7ad3-115">_marcador de posición_</span><span class="sxs-lookup"><span data-stu-id="a7ad3-115">_placeholder_</span></span>
  
> <span data-ttu-id="a7ad3-116">Este miembro está reservado para el uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="a7ad3-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="a7ad3-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="a7ad3-117">_ltid_</span></span>
  
> <span data-ttu-id="a7ad3-118">Identificador a largo plazo de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a7ad3-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7ad3-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7ad3-119">See also</span></span>



[<span data-ttu-id="a7ad3-120">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="a7ad3-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a7ad3-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a7ad3-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a7ad3-122">LTID</span><span class="sxs-lookup"><span data-stu-id="a7ad3-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="a7ad3-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="a7ad3-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="a7ad3-124">Sincronizar</span><span class="sxs-lookup"><span data-stu-id="a7ad3-124">SYNC</span></span>](sync.md)

