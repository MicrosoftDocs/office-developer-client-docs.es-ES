---
title: SYNCSTATE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 63c47e94-f603-aef9-afed-e3819bd79408
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 64348347ea930e6a6a80b9a9075299d2e3109eda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417633"
---
# <a name="syncstate"></a><span data-ttu-id="1591f-103">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="1591f-103">SYNCSTATE</span></span>

<span data-ttu-id="1591f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1591f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1591f-105">Esta estructura define los estados de la máquina de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="1591f-105">This structure defines the states for the replication state machine.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1591f-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="1591f-106">Quick info</span></span>

```cpp
typedef enum { 
    LR_SYNC_IDLE = 0, 
    LR_SYNC, 
    LR_SYNC_UPLOAD_HIERARCHY, 
    LR_SYNC_UPLOAD_FOLDER, 
    LR_SYNC_CONTENTS, 
    LR_SYNC_UPLOAD_TABLE, 
    LR_SYNC_UPLOAD_MESSAGE, 
    LR_SYNC_UPLOAD_MESSAGE_READ = 8, 
    LR_SYNC_UPLOAD_MESSAGE_DEL, 
    LR_SYNC_DOWNLOAD_HIERARCHY, 
    LR_SYNC_DOWNLOAD_TABLE, 
    LR_SYNC_DOWNLOAD_HEADER = 17 
} SYNCSTATE; 

```

## <a name="see-also"></a><span data-ttu-id="1591f-107">Vea también</span><span class="sxs-lookup"><span data-stu-id="1591f-107">See also</span></span>

- [<span data-ttu-id="1591f-108">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="1591f-108">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="1591f-109">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="1591f-109">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="1591f-110">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="1591f-110">MAPI Constants</span></span>](mapi-constants.md)

