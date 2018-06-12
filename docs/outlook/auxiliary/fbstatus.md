---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Una enumeración para el estado libre/ocupado de bloques de libre/ocupado.
ms.openlocfilehash: 67d710f82856dc8ff4839c926018eef88d355f73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816070"
---
# <a name="fbstatus"></a><span data-ttu-id="13bec-103">FBStatus</span><span class="sxs-lookup"><span data-stu-id="13bec-103">FBStatus</span></span>

<span data-ttu-id="13bec-104">Una enumeración para el estado libre/ocupado de bloques de libre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="13bec-104">An enumeration for the free/busy status of free/busy blocks.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="13bec-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="13bec-105">Quick info</span></span>

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a><span data-ttu-id="13bec-106">Notas</span><span class="sxs-lookup"><span data-stu-id="13bec-106">Remarks</span></span>

<span data-ttu-id="13bec-107">El estado de disponibilidad de un bloque de tiempo determina cómo se muestra en un calendario: **libre**, **ocupado**, **provisional**o **Fuera de la oficina**.</span><span class="sxs-lookup"><span data-stu-id="13bec-107">The free/busy status of a block of time determines how it is displayed on a calendar: **Free**, **Busy**, **Tentative**, or **Out of Office**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13bec-108">Ver también</span><span class="sxs-lookup"><span data-stu-id="13bec-108">See also</span></span>

- [<span data-ttu-id="13bec-109">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="13bec-109">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="13bec-110">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="13bec-110">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)

