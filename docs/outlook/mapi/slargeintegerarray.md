---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382732"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="5d1ed-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="5d1ed-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="5d1ed-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d1ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d1ed-105">Contiene una matriz de estructuras [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) que se utilizan para describir una propiedad de tipo PT_MV_I8.</span><span class="sxs-lookup"><span data-stu-id="5d1ed-105">Contains an array of [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d1ed-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5d1ed-106">Header file:</span></span>  <br/> |<span data-ttu-id="5d1ed-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d1ed-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="5d1ed-108">Members</span><span class="sxs-lookup"><span data-stu-id="5d1ed-108">Members</span></span>

 <span data-ttu-id="5d1ed-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="5d1ed-109">**cValues**</span></span>
  
> <span data-ttu-id="5d1ed-110">Recuento de valores de la matriz indicada por el miembro **lpli** .</span><span class="sxs-lookup"><span data-stu-id="5d1ed-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="5d1ed-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="5d1ed-111">**lpli**</span></span>
  
> <span data-ttu-id="5d1ed-112">Puntero a una matriz de estructuras **LARGE_INTEGER** manteniendo los valores enteros.</span><span class="sxs-lookup"><span data-stu-id="5d1ed-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5d1ed-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d1ed-113">Remarks</span></span>

<span data-ttu-id="5d1ed-114">Para obtener más información sobre PT_MV_18, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="5d1ed-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5d1ed-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d1ed-115">See also</span></span>



[<span data-ttu-id="5d1ed-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5d1ed-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="5d1ed-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="5d1ed-117">MAPI Structures</span></span>](mapi-structures.md)

