---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Define un bloque de datos de disponibilidad. Este es un elemento de un calendario representado por una cita o una solicitud de reunión.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413202"
---
# <a name="fbblock_1"></a><span data-ttu-id="a1e6f-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="a1e6f-104">FBBlock_1</span></span>

<span data-ttu-id="a1e6f-105">Define un bloque de datos de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="a1e6f-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="a1e6f-106">Este es un elemento de un calendario representado por una cita o una solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="a1e6f-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a1e6f-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="a1e6f-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="a1e6f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1e6f-108">Members</span></span>

<span data-ttu-id="a1e6f-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="a1e6f-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="a1e6f-110">La hora de inicio del bloque, expresada en tiempo relativo.</span><span class="sxs-lookup"><span data-stu-id="a1e6f-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="a1e6f-111">Para obtener más información, vea [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="a1e6f-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="a1e6f-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="a1e6f-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="a1e6f-113">La hora de finalización del bloque, expresada en tiempo relativo.</span><span class="sxs-lookup"><span data-stu-id="a1e6f-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="a1e6f-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="a1e6f-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="a1e6f-115">El estado de disponibilidad de este bloque, que indica si el usuario está fuera de la oficina, ocupado, provisional o gratuito, durante el período de tiempo entre  _m_tmStart_ y  _m_tmEnd_.</span><span class="sxs-lookup"><span data-stu-id="a1e6f-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1e6f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1e6f-116">See also</span></span>

- [<span data-ttu-id="a1e6f-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="a1e6f-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="a1e6f-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="a1e6f-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="a1e6f-119">Utilizar un tiempo relativo a los datos de disponibilidad de acceso</span><span class="sxs-lookup"><span data-stu-id="a1e6f-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

