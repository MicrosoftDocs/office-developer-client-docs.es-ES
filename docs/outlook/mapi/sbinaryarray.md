---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351061"
---
# <a name="sbinaryarray"></a><span data-ttu-id="2fe8c-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="2fe8c-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="2fe8c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fe8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fe8c-105">Contiene una matriz de valores binarios.</span><span class="sxs-lookup"><span data-stu-id="2fe8c-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2fe8c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2fe8c-106">Header file:</span></span>  <br/> |<span data-ttu-id="2fe8c-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2fe8c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="2fe8c-108">Members</span><span class="sxs-lookup"><span data-stu-id="2fe8c-108">Members</span></span>

 <span data-ttu-id="2fe8c-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="2fe8c-109">**cValues**</span></span>
  
> <span data-ttu-id="2fe8c-110">Número de valores de la matriz a los que señala el miembro **lpbin** .</span><span class="sxs-lookup"><span data-stu-id="2fe8c-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="2fe8c-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="2fe8c-111">**lpbin**</span></span>
  
> <span data-ttu-id="2fe8c-112">Puntero a una matriz de estructuras [SBinary](sbinary.md) que contiene los valores binarios.</span><span class="sxs-lookup"><span data-stu-id="2fe8c-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2fe8c-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2fe8c-113">Remarks</span></span>

<span data-ttu-id="2fe8c-114">La estructura **SBinaryArray** se usa para describir propiedades de tipo PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="2fe8c-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="2fe8c-115">Para obtener más información acerca de PT_MV_BINARY, vea [lista de tipos de propiedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="2fe8c-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2fe8c-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fe8c-116">See also</span></span>



[<span data-ttu-id="2fe8c-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="2fe8c-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="2fe8c-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2fe8c-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2fe8c-119">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="2fe8c-119">MAPI Structures</span></span>](mapi-structures.md)

