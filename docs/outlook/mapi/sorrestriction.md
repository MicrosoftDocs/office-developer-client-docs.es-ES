---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 054625601b496a8ec8f7745aa4cbc4715eed81a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585062"
---
# <a name="sorrestriction"></a><span data-ttu-id="af40c-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="af40c-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="af40c-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af40c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af40c-105">Describe una restricción **o** que se usa para aplicar una operación **OR** lógica para una restricción.</span><span class="sxs-lookup"><span data-stu-id="af40c-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af40c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="af40c-106">Header file:</span></span>  <br/> |<span data-ttu-id="af40c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af40c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="af40c-108">Members</span><span class="sxs-lookup"><span data-stu-id="af40c-108">Members</span></span>

 <span data-ttu-id="af40c-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="af40c-109">**cRes**</span></span>
  
> <span data-ttu-id="af40c-110">Recuento de las estructuras de la matriz indicada por el miembro **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="af40c-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="af40c-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="af40c-111">**lpRes**</span></span>
  
> <span data-ttu-id="af40c-112">Puntero a la estructura de [SRestriction](srestriction.md) que describe la restricción de combinarse mediante la operación de **OR** lógica.</span><span class="sxs-lookup"><span data-stu-id="af40c-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="af40c-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af40c-113">Remarks</span></span>

<span data-ttu-id="af40c-114">Para obtener más información acerca de la estructura **SOrRestriction** , vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="af40c-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af40c-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="af40c-115">See also</span></span>



[<span data-ttu-id="af40c-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="af40c-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="af40c-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="af40c-117">MAPI Structures</span></span>](mapi-structures.md)

