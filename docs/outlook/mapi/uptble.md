---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 62c18ac609547563ad0e98cbd914866e05888ac8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820954"
---
# <a name="uptble"></a><span data-ttu-id="58c6d-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="58c6d-103">UPTBLE</span></span>

<span data-ttu-id="58c6d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58c6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58c6d-105">Información extendida para cargar el contenido de una carpeta durante la [carga de estado de la tabla](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="58c6d-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="58c6d-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="58c6d-106">Quick info</span></span>

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="58c6d-107">Members</span><span class="sxs-lookup"><span data-stu-id="58c6d-107">Members</span></span>

 <span data-ttu-id="58c6d-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="58c6d-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="58c6d-109">[out] Índice que se va a realizar un seguimiento de cargar el número de _cEntMod_ de elementos nuevos o modificados.</span><span class="sxs-lookup"><span data-stu-id="58c6d-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="58c6d-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="58c6d-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="58c6d-111">[out] Número de elementos nuevos o modificados en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="58c6d-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="58c6d-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="58c6d-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="58c6d-113">[out] Para realizar un seguimiento de cargar el número de _cEntRead_ leer elementos de índice.</span><span class="sxs-lookup"><span data-stu-id="58c6d-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="58c6d-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="58c6d-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="58c6d-115">[out] Número de elementos de lectura en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="58c6d-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="58c6d-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="58c6d-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="58c6d-117">[out] Índice que se va a realizar un seguimiento de cargar el número de _cEntDel_ elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="58c6d-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="58c6d-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="58c6d-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="58c6d-119">[out] Número de elementos eliminados en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="58c6d-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="58c6d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="58c6d-120">See also</span></span>

- [<span data-ttu-id="58c6d-121">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="58c6d-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="58c6d-122">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="58c6d-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="58c6d-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="58c6d-123">UPTBL</span></span>](uptbl.md)

