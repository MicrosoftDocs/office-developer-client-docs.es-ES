---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429876"
---
# <a name="srealarray"></a><span data-ttu-id="17d02-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="17d02-103">SRealArray</span></span>

  
  
<span data-ttu-id="17d02-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17d02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17d02-105">Contiene una matriz de valores float que se usan para describir una propiedad de tipo PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="17d02-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17d02-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="17d02-106">Header file:</span></span>  <br/> |<span data-ttu-id="17d02-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="17d02-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="17d02-108">Members</span><span class="sxs-lookup"><span data-stu-id="17d02-108">Members</span></span>

 <span data-ttu-id="17d02-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="17d02-109">**cValues**</span></span>
  
> <span data-ttu-id="17d02-110">Número de valores de la matriz a los que señala el miembro **lpflt** .</span><span class="sxs-lookup"><span data-stu-id="17d02-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="17d02-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="17d02-111">**lpflt**</span></span>
  
> <span data-ttu-id="17d02-112">Puntero a una matriz de valores float.</span><span class="sxs-lookup"><span data-stu-id="17d02-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17d02-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17d02-113">Remarks</span></span>

<span data-ttu-id="17d02-114">Para obtener más información sobre el tipo de propiedad PT_MV_R4, vea [tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="17d02-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="17d02-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="17d02-115">See also</span></span>



[<span data-ttu-id="17d02-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="17d02-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="17d02-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="17d02-117">MAPI Structures</span></span>](mapi-structures.md)

