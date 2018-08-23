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
ms.openlocfilehash: 9495caecd514656f6fd62fb5db6cd8ac2faf4b50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581744"
---
# <a name="indexsearchpusherprocess"></a><span data-ttu-id="70cf9-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="70cf9-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="70cf9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70cf9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70cf9-105">Especifica el proceso es enviar una notificación para que el controlador de protocolo MAPI que está listo para la indización de un objeto de ese almacén.</span><span class="sxs-lookup"><span data-stu-id="70cf9-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="70cf9-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="70cf9-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="70cf9-107">Members</span><span class="sxs-lookup"><span data-stu-id="70cf9-107">Members</span></span>

 <span data-ttu-id="70cf9-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="70cf9-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="70cf9-109">Identificador de proceso para el proceso que envía una notificación de indización para el indizador del controlador de protocolo MAPI.</span><span class="sxs-lookup"><span data-stu-id="70cf9-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

