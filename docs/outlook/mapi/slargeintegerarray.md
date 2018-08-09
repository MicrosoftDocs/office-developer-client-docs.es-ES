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
ms.openlocfilehash: 4d6785783f69857bd93f3c5818983e832e16af05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820705"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="3219d-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="3219d-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="3219d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3219d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3219d-105">Contiene una matriz de estructuras [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) que se utilizan para describir una propiedad de tipo PT_MV_I8.</span><span class="sxs-lookup"><span data-stu-id="3219d-105">Contains an array of [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3219d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="3219d-106">Header file:</span></span>  <br/> |<span data-ttu-id="3219d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3219d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="3219d-108">Members</span><span class="sxs-lookup"><span data-stu-id="3219d-108">Members</span></span>

 <span data-ttu-id="3219d-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="3219d-109">**cValues**</span></span>
  
> <span data-ttu-id="3219d-110">Recuento de valores de la matriz indicada por el miembro **lpli** .</span><span class="sxs-lookup"><span data-stu-id="3219d-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="3219d-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="3219d-111">**lpli**</span></span>
  
> <span data-ttu-id="3219d-112">Puntero a una matriz de estructuras **LARGE_INTEGER** manteniendo los valores enteros.</span><span class="sxs-lookup"><span data-stu-id="3219d-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3219d-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3219d-113">Remarks</span></span>

<span data-ttu-id="3219d-114">Para obtener más información sobre PT_MV_18, vea la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="3219d-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3219d-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="3219d-115">See also</span></span>



[<span data-ttu-id="3219d-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3219d-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3219d-117">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="3219d-117">MAPI Structures</span></span>](mapi-structures.md)

