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
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437934"
---
# <a name="sorrestriction"></a><span data-ttu-id="8e5aa-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="8e5aa-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="8e5aa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e5aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e5aa-105">Describe una restricción **OR** que se usa para aplicar una operación **OR** lógica a una restricción.</span><span class="sxs-lookup"><span data-stu-id="8e5aa-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e5aa-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8e5aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="8e5aa-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e5aa-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="8e5aa-108">Members</span><span class="sxs-lookup"><span data-stu-id="8e5aa-108">Members</span></span>

 <span data-ttu-id="8e5aa-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="8e5aa-109">**cRes**</span></span>
  
> <span data-ttu-id="8e5aa-110">Recuento de estructuras en la matriz a la que apunta el **miembro lpRes.**</span><span class="sxs-lookup"><span data-stu-id="8e5aa-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="8e5aa-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="8e5aa-111">**lpRes**</span></span>
  
> <span data-ttu-id="8e5aa-112">Puntero a la [estructura SRestriction](srestriction.md) que describe la restricción que se unirá mediante la operación **LÓGICA OR.**</span><span class="sxs-lookup"><span data-stu-id="8e5aa-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8e5aa-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e5aa-113">Remarks</span></span>

<span data-ttu-id="8e5aa-114">Para obtener más información acerca **de la estructura SOrRestriction,** vea [About Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="8e5aa-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e5aa-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e5aa-115">See also</span></span>



[<span data-ttu-id="8e5aa-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="8e5aa-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="8e5aa-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="8e5aa-117">MAPI Structures</span></span>](mapi-structures.md)

