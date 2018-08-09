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
ms.openlocfilehash: 3fd61828cd631c4abc0131da867ca213a3c44d20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820751"
---
# <a name="spropproblemarray"></a><span data-ttu-id="0e006-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0e006-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="0e006-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e006-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e006-105">Contiene una matriz de uno o más estructuras [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="0e006-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e006-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0e006-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e006-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e006-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0e006-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="0e006-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="0e006-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0e006-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="0e006-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0e006-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="0e006-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0e006-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="0e006-112">Members</span><span class="sxs-lookup"><span data-stu-id="0e006-112">Members</span></span>

 <span data-ttu-id="0e006-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="0e006-113">**cProblem**</span></span>
  
> <span data-ttu-id="0e006-114">Recuento de las estructuras de [SPropProblem](spropproblem.md) en la matriz indicada por el miembro **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="0e006-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="0e006-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="0e006-115">**aProblem**</span></span>
  
> <span data-ttu-id="0e006-116">Matriz de estructuras **SPropProblem** , que describe un error de propiedad.</span><span class="sxs-lookup"><span data-stu-id="0e006-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0e006-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e006-117">Remarks</span></span>

<span data-ttu-id="0e006-118">Para obtener más información acerca de cómo funcionan las estructuras **SPropProblem** y **SPropProblemArray** con errores relacionados con las propiedades, vea [Propiedades de nombre de MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="0e006-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0e006-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e006-119">See also</span></span>



[<span data-ttu-id="0e006-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="0e006-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="0e006-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="0e006-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="0e006-122">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="0e006-122">MAPI Structures</span></span>](mapi-structures.md)

