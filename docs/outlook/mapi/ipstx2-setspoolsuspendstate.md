---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e988114e8e71ad1f80d20ab0d5a30c37425f5952
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407518"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="46644-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="46644-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="46644-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46644-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46644-105">Establece el estado suspendido en la cola.</span><span class="sxs-lookup"><span data-stu-id="46644-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="46644-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46644-106">Parameters</span></span>

 <span data-ttu-id="46644-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="46644-107">_ulState_</span></span>
  
> <span data-ttu-id="46644-108">[entrada] Estado en el que se va a establecer la cola.</span><span class="sxs-lookup"><span data-stu-id="46644-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="46644-109">Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="46644-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="46644-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="46644-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="46644-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="46644-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="46644-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="46644-112">See also</span></span>



[<span data-ttu-id="46644-113">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="46644-113">MAPI Constants</span></span>](mapi-constants.md)

