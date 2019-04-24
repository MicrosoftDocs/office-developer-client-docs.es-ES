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
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329711"
---
# <a name="uptble"></a><span data-ttu-id="a2500-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="a2500-103">UPTBLE</span></span>

<span data-ttu-id="a2500-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2500-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2500-105">Información extendida para cargar el contenido de una carpeta durante el [Estado de carga](upload-table-state.md)de la tabla.</span><span class="sxs-lookup"><span data-stu-id="a2500-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a2500-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="a2500-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="a2500-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2500-107">Members</span></span>

 <span data-ttu-id="a2500-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="a2500-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="a2500-109">contempla Índice para realizar un seguimiento de la carga del _cEntMod_ número de elementos nuevos o modificados.</span><span class="sxs-lookup"><span data-stu-id="a2500-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="a2500-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="a2500-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="a2500-111">contempla Número de elementos nuevos o modificados de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2500-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="a2500-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="a2500-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="a2500-113">contempla Índice para realizar un seguimiento de la carga del número de elementos leídos de _cEntRead_ .</span><span class="sxs-lookup"><span data-stu-id="a2500-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="a2500-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="a2500-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="a2500-115">contempla Número de elementos leídos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2500-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="a2500-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="a2500-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="a2500-117">contempla Índice para realizar un seguimiento de la carga del número de elementos eliminados de _cEntDel_ .</span><span class="sxs-lookup"><span data-stu-id="a2500-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="a2500-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="a2500-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="a2500-119">contempla Número de elementos eliminados de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2500-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a2500-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2500-120">See also</span></span>

- [<span data-ttu-id="a2500-121">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="a2500-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="a2500-122">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="a2500-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="a2500-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="a2500-123">UPTBL</span></span>](uptbl.md)

