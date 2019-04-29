---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 07a1a0a1953d136da534fbdc6339d326c877bebf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426656"
---
# <a name="snotrestriction"></a><span data-ttu-id="c9dc1-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="c9dc1-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="c9dc1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9dc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9dc1-105">Describe una restricción **Not** , que se usa para aplicar una operación **Not** lógica a una restricción.</span><span class="sxs-lookup"><span data-stu-id="c9dc1-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9dc1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c9dc1-106">Header file:</span></span>  <br/> |<span data-ttu-id="c9dc1-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c9dc1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="c9dc1-108">Members</span><span class="sxs-lookup"><span data-stu-id="c9dc1-108">Members</span></span>

 <span data-ttu-id="c9dc1-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="c9dc1-109">**ulReserved**</span></span>
  
> <span data-ttu-id="c9dc1-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c9dc1-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c9dc1-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="c9dc1-111">**lpRes**</span></span>
  
> <span data-ttu-id="c9dc1-112">Puntero a una estructura [SRestriction](srestriction.md) que describe la restricción que se va a unir al operador **Not** lógico.</span><span class="sxs-lookup"><span data-stu-id="c9dc1-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c9dc1-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9dc1-113">Remarks</span></span>

<span data-ttu-id="c9dc1-114">Para obtener más información acerca de la estructura **SNotRestriction** , consulte [About Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="c9dc1-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c9dc1-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="c9dc1-115">See also</span></span>



[<span data-ttu-id="c9dc1-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="c9dc1-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="c9dc1-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="c9dc1-117">MAPI Structures</span></span>](mapi-structures.md)

