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
ms.openlocfilehash: 24e16aeb1bbee1c35cf8fbd5813fb3e83b762187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818258"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="a31c7-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="a31c7-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="a31c7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a31c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a31c7-105">La estructura se utiliza con [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="a31c7-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="a31c7-106">Members</span><span class="sxs-lookup"><span data-stu-id="a31c7-106">Members</span></span>

 <span data-ttu-id="a31c7-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="a31c7-107">**ulSize**</span></span>
  
> <span data-ttu-id="a31c7-108">El tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="a31c7-108">The size of the structure.</span></span>
    
 <span data-ttu-id="a31c7-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="a31c7-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="a31c7-110">Un puntero al objeto IUnknown en el que se vaya a agregar este objeto.</span><span class="sxs-lookup"><span data-stu-id="a31c7-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="a31c7-111">Esto permite que las llamadas QueryInterface pase al objeto creado.</span><span class="sxs-lookup"><span data-stu-id="a31c7-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="a31c7-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="a31c7-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="a31c7-113">Debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a31c7-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a31c7-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="a31c7-114">See also</span></span>



[<span data-ttu-id="a31c7-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="a31c7-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="a31c7-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="a31c7-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

