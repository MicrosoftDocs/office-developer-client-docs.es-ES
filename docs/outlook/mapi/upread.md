---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7338edc13227e303ec5fa47da4a5d9ee611c6749
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419887"
---
# <a name="upread"></a><span data-ttu-id="20939-103">UPREAD</span><span class="sxs-lookup"><span data-stu-id="20939-103">UPREAD</span></span>

  
  
<span data-ttu-id="20939-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20939-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20939-105">Información para cargar el estado de lectura de los elementos durante el [Estado de lectura](upload-read-status-state.md)de la carga.</span><span class="sxs-lookup"><span data-stu-id="20939-105">Information for uploading the read state of items during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="20939-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="20939-106">Quick info</span></span>

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="20939-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="20939-107">Members</span></span>

 <span data-ttu-id="20939-108">_pupre_</span><span class="sxs-lookup"><span data-stu-id="20939-108">_pupre_</span></span>
  
>  <span data-ttu-id="20939-109">contempla Vector de las entradas que se han **[leído](upreade.md)** .</span><span class="sxs-lookup"><span data-stu-id="20939-109">[out] Vector of **[UPREADE](upreade.md)** entries.</span></span> 
    
 <span data-ttu-id="20939-110">_Ciento_</span><span class="sxs-lookup"><span data-stu-id="20939-110">_cEnt_</span></span>
  
>  <span data-ttu-id="20939-111">contempla Número de entradas que se han **leído** .</span><span class="sxs-lookup"><span data-stu-id="20939-111">[out] Number of **UPREADE** entries.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="20939-112">Ver también</span><span class="sxs-lookup"><span data-stu-id="20939-112">See also</span></span>



[<span data-ttu-id="20939-113">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="20939-113">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="20939-114">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="20939-114">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="20939-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="20939-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="20939-116">UPREADE</span><span class="sxs-lookup"><span data-stu-id="20939-116">UPREADE</span></span>](upreade.md)

