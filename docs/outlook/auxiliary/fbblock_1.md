---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Define un bloque libre/ocupado de datos. Esto es un elemento en un calendario representado por una convocatoria de reunión o cita.
ms.openlocfilehash: 93418e3777e9d9f0a016822ea5897b8fccc37ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816059"
---
# <a name="fbblock1"></a><span data-ttu-id="1d800-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="1d800-104">FBBlock_1</span></span>

<span data-ttu-id="1d800-105">Define un bloque libre/ocupado de datos.</span><span class="sxs-lookup"><span data-stu-id="1d800-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="1d800-106">Esto es un elemento en un calendario representado por una convocatoria de reunión o cita.</span><span class="sxs-lookup"><span data-stu-id="1d800-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1d800-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="1d800-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="1d800-108">Members</span><span class="sxs-lookup"><span data-stu-id="1d800-108">Members</span></span>

<span data-ttu-id="1d800-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="1d800-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="1d800-110">La hora de inicio para el bloque, expresado en hora relativa.</span><span class="sxs-lookup"><span data-stu-id="1d800-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="1d800-111">Para obtener más información, vea [usar la hora relativa para tener acceso a datos de disponibilidad](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="1d800-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="1d800-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="1d800-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="1d800-113">La hora de finalización para el bloque, expresado en hora relativa.</span><span class="sxs-lookup"><span data-stu-id="1d800-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="1d800-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="1d800-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="1d800-115">El estado de disponibilidad de este bloque, que indica si el usuario está fuera de la oficina, ocupado, provisional o libre, durante el período de tiempo entre _m_tmStart_ y _m_tmEnd_.</span><span class="sxs-lookup"><span data-stu-id="1d800-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d800-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d800-116">See also</span></span>

- [<span data-ttu-id="1d800-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="1d800-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="1d800-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="1d800-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="1d800-119">Utilizar un tiempo relativo a los datos de disponibilidad de acceso</span><span class="sxs-lookup"><span data-stu-id="1d800-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

