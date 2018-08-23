---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: eb182d9cc51c196558f9e9192a65352e87372bf0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582521"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="74261-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="74261-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="74261-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74261-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74261-105">La estructura se utiliza con [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="74261-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="74261-106">Members</span><span class="sxs-lookup"><span data-stu-id="74261-106">Members</span></span>

 <span data-ttu-id="74261-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="74261-107">**ulSize**</span></span>
  
> <span data-ttu-id="74261-108">El tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="74261-108">The size of the structure.</span></span>
    
 <span data-ttu-id="74261-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="74261-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="74261-110">Un puntero al objeto IUnknown en el que se vaya a agregar este objeto.</span><span class="sxs-lookup"><span data-stu-id="74261-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="74261-111">Esto permite que las llamadas QueryInterface pase al objeto creado.</span><span class="sxs-lookup"><span data-stu-id="74261-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="74261-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="74261-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="74261-113">Debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="74261-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74261-114">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="74261-114">See also</span></span>



[<span data-ttu-id="74261-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="74261-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="74261-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="74261-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

