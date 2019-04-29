---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406860"
---
# <a name="spropproblemarray"></a><span data-ttu-id="6947c-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="6947c-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="6947c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6947c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6947c-105">Contiene una matriz de una o varias estructuras [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="6947c-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6947c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6947c-106">Header file:</span></span>  <br/> |<span data-ttu-id="6947c-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6947c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6947c-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="6947c-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="6947c-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="6947c-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="6947c-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="6947c-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="6947c-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="6947c-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="6947c-112">Members</span><span class="sxs-lookup"><span data-stu-id="6947c-112">Members</span></span>

 <span data-ttu-id="6947c-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="6947c-113">**cProblem**</span></span>
  
> <span data-ttu-id="6947c-114">Número de estructuras [SPropProblem](spropproblem.md) en la matriz indicada por el miembro **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="6947c-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="6947c-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="6947c-115">**aProblem**</span></span>
  
> <span data-ttu-id="6947c-116">Matriz de estructuras **SPropProblem** , cada una de las cuales describe un error de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6947c-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6947c-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6947c-117">Remarks</span></span>

<span data-ttu-id="6947c-118">Para obtener más información sobre cómo funcionan las estructuras **SPropProblem** y **SPropProblemArray** con errores relacionados con las propiedades, consulte [MAPI con nombre de propiedades](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="6947c-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6947c-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="6947c-119">See also</span></span>



[<span data-ttu-id="6947c-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="6947c-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="6947c-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="6947c-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="6947c-122">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="6947c-122">MAPI Structures</span></span>](mapi-structures.md)

