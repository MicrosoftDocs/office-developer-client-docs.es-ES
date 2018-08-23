---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6986ed7c9ab9932c5d95fcfb7f74f80088f21971
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580372"
---
# <a name="sdoublearray"></a><span data-ttu-id="d78f1-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="d78f1-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="d78f1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d78f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d78f1-105">Contiene una matriz de tipo Double que se usa para describir una propiedad de tipo PT_MV_DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="d78f1-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d78f1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d78f1-106">Header file:</span></span>  <br/> |<span data-ttu-id="d78f1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d78f1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="d78f1-108">Members</span><span class="sxs-lookup"><span data-stu-id="d78f1-108">Members</span></span>

 <span data-ttu-id="d78f1-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d78f1-109">**cValues**</span></span>
  
> <span data-ttu-id="d78f1-110">Recuento de valores de la matriz indicada por el miembro **lpdbl** .</span><span class="sxs-lookup"><span data-stu-id="d78f1-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="d78f1-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="d78f1-111">**lpdbl**</span></span>
  
> <span data-ttu-id="d78f1-112">Puntero a una matriz de valores de tipo double.</span><span class="sxs-lookup"><span data-stu-id="d78f1-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d78f1-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d78f1-113">Remarks</span></span>

<span data-ttu-id="d78f1-114">Para obtener más información sobre PT_MV_DOUBLE, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="d78f1-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d78f1-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d78f1-115">See also</span></span>



[<span data-ttu-id="d78f1-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d78f1-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d78f1-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d78f1-117">MAPI Structures</span></span>](mapi-structures.md)

