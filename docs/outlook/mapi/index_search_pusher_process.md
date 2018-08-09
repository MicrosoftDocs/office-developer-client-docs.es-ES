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
ms.openlocfilehash: ada6d4127d503aae0b068d40d2bb48cb6b833ea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817813"
---
# <a name="indexsearchpusherprocess"></a><span data-ttu-id="2dd3a-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="2dd3a-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="2dd3a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2dd3a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2dd3a-105">Especifica el proceso es enviar una notificación para que el controlador de protocolo MAPI que está listo para la indización de un objeto de ese almacén.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2dd3a-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="2dd3a-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="2dd3a-107">Members</span><span class="sxs-lookup"><span data-stu-id="2dd3a-107">Members</span></span>

 <span data-ttu-id="2dd3a-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="2dd3a-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="2dd3a-109">Identificador de proceso para el proceso que envía una notificación de indización para el indizador del controlador de protocolo MAPI.</span><span class="sxs-lookup"><span data-stu-id="2dd3a-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

