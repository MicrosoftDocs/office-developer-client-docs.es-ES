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
ms.openlocfilehash: 30ec82788e46ca07c6529ce74872e0a0c7c012a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817935"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="a7aba-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="a7aba-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="a7aba-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7aba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7aba-105">Establece el estado de suspensión de la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="a7aba-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="a7aba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7aba-106">Parameters</span></span>

 <span data-ttu-id="a7aba-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="a7aba-107">_ulState_</span></span>
  
> <span data-ttu-id="a7aba-108">[entrada] Para establecer la cola de impresión en el estado.</span><span class="sxs-lookup"><span data-stu-id="a7aba-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="a7aba-109">Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="a7aba-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="a7aba-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="a7aba-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="a7aba-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="a7aba-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="a7aba-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7aba-112">See also</span></span>



[<span data-ttu-id="a7aba-113">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a7aba-113">MAPI Constants</span></span>](mapi-constants.md)
