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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413843"
---
# <a name="uptble"></a><span data-ttu-id="7edbc-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="7edbc-103">UPTBLE</span></span>

<span data-ttu-id="7edbc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7edbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7edbc-105">Información extendida para cargar el contenido de una carpeta durante el estado [de la tabla de carga.](upload-table-state.md)</span><span class="sxs-lookup"><span data-stu-id="7edbc-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7edbc-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="7edbc-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="7edbc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7edbc-107">Members</span></span>

 <span data-ttu-id="7edbc-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="7edbc-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="7edbc-109">[salida] Índice para realizar un seguimiento de la  _carga del número cEntMod_ de elementos nuevos o modificados.</span><span class="sxs-lookup"><span data-stu-id="7edbc-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="7edbc-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="7edbc-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="7edbc-111">[salida] Número de elementos nuevos o modificados de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="7edbc-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="7edbc-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="7edbc-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="7edbc-113">[salida] Índice para realizar un seguimiento de la carga del número de elementos de lectura _cEntRead._</span><span class="sxs-lookup"><span data-stu-id="7edbc-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="7edbc-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="7edbc-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="7edbc-115">[salida] Número de elementos leídos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="7edbc-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="7edbc-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="7edbc-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="7edbc-117">[salida] Índice para realizar un seguimiento de la carga del número _de elementos eliminados de cEntDel._</span><span class="sxs-lookup"><span data-stu-id="7edbc-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="7edbc-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="7edbc-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="7edbc-119">[salida] Número de elementos eliminados en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="7edbc-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7edbc-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7edbc-120">See also</span></span>

- [<span data-ttu-id="7edbc-121">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="7edbc-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="7edbc-122">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="7edbc-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="7edbc-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="7edbc-123">UPTBL</span></span>](uptbl.md)

