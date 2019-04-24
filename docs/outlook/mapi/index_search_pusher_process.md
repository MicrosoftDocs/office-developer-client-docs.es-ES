---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 64e5cf31dffdc794a22bcbd6d503a2b688f9c733
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332210"
---
# <a name="indexsearchpusherprocess"></a><span data-ttu-id="e432c-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="e432c-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="e432c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e432c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e432c-105">Especifica el proceso que envía una notificación al controlador de protocolo MAPI que un objeto de ese almacén está preparado para la indización.</span><span class="sxs-lookup"><span data-stu-id="e432c-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e432c-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e432c-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="e432c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e432c-107">Members</span></span>

 <span data-ttu-id="e432c-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="e432c-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="e432c-109">IDENTIFICADOR de proceso del proceso que envía una notificación de indización al indizador del controlador de protocolo MAPI.</span><span class="sxs-lookup"><span data-stu-id="e432c-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

