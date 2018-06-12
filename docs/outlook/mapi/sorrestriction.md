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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 06b9b6a046aaa0f16418f75d402cc5be44f845a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820728"
---
# <a name="sorrestriction"></a><span data-ttu-id="bdc07-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="bdc07-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="bdc07-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bdc07-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bdc07-105">Describe una restricción **o** que se usa para aplicar una operación **OR** lógica para una restricción.</span><span class="sxs-lookup"><span data-stu-id="bdc07-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bdc07-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="bdc07-106">Header file:</span></span>  <br/> |<span data-ttu-id="bdc07-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bdc07-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="bdc07-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="bdc07-108">Members</span></span>

 <span data-ttu-id="bdc07-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="bdc07-109">**cRes**</span></span>
  
> <span data-ttu-id="bdc07-110">Recuento de las estructuras de la matriz indicada por el miembro **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="bdc07-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="bdc07-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="bdc07-111">**lpRes**</span></span>
  
> <span data-ttu-id="bdc07-112">Puntero a la estructura de [SRestriction](srestriction.md) que describe la restricción de combinarse mediante la operación de **OR** lógica.</span><span class="sxs-lookup"><span data-stu-id="bdc07-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bdc07-113">Notas</span><span class="sxs-lookup"><span data-stu-id="bdc07-113">Remarks</span></span>

<span data-ttu-id="bdc07-114">Para obtener más información acerca de la estructura **SOrRestriction** , vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="bdc07-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bdc07-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="bdc07-115">See also</span></span>



[<span data-ttu-id="bdc07-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="bdc07-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="bdc07-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="bdc07-117">MAPI Structures</span></span>](mapi-structures.md)

