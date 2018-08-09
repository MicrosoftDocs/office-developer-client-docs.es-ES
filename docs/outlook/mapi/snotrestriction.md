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
ms.openlocfilehash: a07a7737e9b9354514a2d5ac2ec37a393a3cd4e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820720"
---
# <a name="snotrestriction"></a><span data-ttu-id="b6894-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="b6894-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="b6894-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6894-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6894-105">Describe una restricción **no** , que se usa para aplicar una operación **NOT** lógica a una restricción.</span><span class="sxs-lookup"><span data-stu-id="b6894-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6894-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b6894-106">Header file:</span></span>  <br/> |<span data-ttu-id="b6894-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6894-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="b6894-108">Members</span><span class="sxs-lookup"><span data-stu-id="b6894-108">Members</span></span>

 <span data-ttu-id="b6894-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="b6894-109">**ulReserved**</span></span>
  
> <span data-ttu-id="b6894-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b6894-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b6894-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="b6894-111">**lpRes**</span></span>
  
> <span data-ttu-id="b6894-112">Puntero a una estructura de [SRestriction](srestriction.md) que describa la restricción esté unido al operador **NOT** lógico.</span><span class="sxs-lookup"><span data-stu-id="b6894-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b6894-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6894-113">Remarks</span></span>

<span data-ttu-id="b6894-114">Para obtener más información acerca de la estructura **SNotRestriction** , vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="b6894-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6894-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6894-115">See also</span></span>



[<span data-ttu-id="b6894-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="b6894-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="b6894-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="b6894-117">MAPI Structures</span></span>](mapi-structures.md)

