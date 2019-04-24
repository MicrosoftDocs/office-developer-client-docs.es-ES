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
ms.openlocfilehash: 91440d619c8ad8a64b2bac7463a26d9c196a3c0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339735"
---
# <a name="sdoublearray"></a><span data-ttu-id="88745-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="88745-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="88745-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88745-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88745-105">Contiene una matriz de doubles que se usa para describir una propiedad de tipo PT_MV_DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="88745-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88745-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="88745-106">Header file:</span></span>  <br/> |<span data-ttu-id="88745-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="88745-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="88745-108">Members</span><span class="sxs-lookup"><span data-stu-id="88745-108">Members</span></span>

 <span data-ttu-id="88745-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="88745-109">**cValues**</span></span>
  
> <span data-ttu-id="88745-110">Número de valores de la matriz a los que señala el miembro **lpdbl** .</span><span class="sxs-lookup"><span data-stu-id="88745-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="88745-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="88745-111">**lpdbl**</span></span>
  
> <span data-ttu-id="88745-112">Puntero a una matriz de valores de tipo Double.</span><span class="sxs-lookup"><span data-stu-id="88745-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="88745-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88745-113">Remarks</span></span>

<span data-ttu-id="88745-114">Para obtener más información acerca de PT_MV_DOUBLE, vea [lista de tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="88745-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="88745-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="88745-115">See also</span></span>



[<span data-ttu-id="88745-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="88745-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="88745-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="88745-117">MAPI Structures</span></span>](mapi-structures.md)

