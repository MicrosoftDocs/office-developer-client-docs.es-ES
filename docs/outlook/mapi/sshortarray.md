---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344502"
---
# <a name="sshortarray"></a><span data-ttu-id="d49fa-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="d49fa-103">SShortArray</span></span>

  
  
<span data-ttu-id="d49fa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d49fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d49fa-105">Contiene una matriz de valores enteros sin signo que se usan para describir una propiedad de tipo PT_MV_SHORT.</span><span class="sxs-lookup"><span data-stu-id="d49fa-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d49fa-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d49fa-106">Header file:</span></span>  <br/> |<span data-ttu-id="d49fa-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d49fa-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="d49fa-108">Members</span><span class="sxs-lookup"><span data-stu-id="d49fa-108">Members</span></span>

 <span data-ttu-id="d49fa-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d49fa-109">**cValues**</span></span>
  
> <span data-ttu-id="d49fa-110">Número de valores de la matriz a los que señala el miembro **LPP** .</span><span class="sxs-lookup"><span data-stu-id="d49fa-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="d49fa-111">**LPP**</span><span class="sxs-lookup"><span data-stu-id="d49fa-111">**lpi**</span></span>
  
> <span data-ttu-id="d49fa-112">Puntero a una matriz de valores enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="d49fa-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d49fa-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d49fa-113">Remarks</span></span>

<span data-ttu-id="d49fa-114">Para obtener más información sobre PT_MV_SHORT y otros tipos de propiedades, consulte [Property Types](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="d49fa-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d49fa-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="d49fa-115">See also</span></span>



[<span data-ttu-id="d49fa-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d49fa-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d49fa-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d49fa-117">MAPI Structures</span></span>](mapi-structures.md)

