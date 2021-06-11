---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438886"
---
# <a name="sandrestriction"></a><span data-ttu-id="dd37c-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="dd37c-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="dd37c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd37c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd37c-105">Describe una restricción **AND,** que se usa para unirse a un grupo de restricciones mediante una operación **AND** lógica.</span><span class="sxs-lookup"><span data-stu-id="dd37c-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd37c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="dd37c-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd37c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dd37c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="dd37c-108">Members</span><span class="sxs-lookup"><span data-stu-id="dd37c-108">Members</span></span>

 <span data-ttu-id="dd37c-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="dd37c-109">**cRes**</span></span>
  
> <span data-ttu-id="dd37c-110">Recuento de restricciones de búsqueda en la matriz señalada por el **miembro lpRes.**</span><span class="sxs-lookup"><span data-stu-id="dd37c-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="dd37c-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="dd37c-111">**lpRes**</span></span>
  
> <span data-ttu-id="dd37c-112">Puntero a una matriz de [estructuras SRestriction](srestriction.md) que se combinarán con una operación **AND** lógica.</span><span class="sxs-lookup"><span data-stu-id="dd37c-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dd37c-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd37c-113">Remarks</span></span>

<span data-ttu-id="dd37c-114">El resultado de **SAndRestriction** es TRUE si todas sus restricciones secundarias se evalúan como TRUE.</span><span class="sxs-lookup"><span data-stu-id="dd37c-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="dd37c-115">Es FALSE si cualquier restricción secundaria se evalúa como FALSE.</span><span class="sxs-lookup"><span data-stu-id="dd37c-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="dd37c-116">Para obtener una descripción de los tipos de restricciones, cómo compilarlas y código de ejemplo, vea [Acerca de las restricciones](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="dd37c-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dd37c-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd37c-117">See also</span></span>



[<span data-ttu-id="dd37c-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="dd37c-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="dd37c-119">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="dd37c-119">MAPI Structures</span></span>](mapi-structures.md)

