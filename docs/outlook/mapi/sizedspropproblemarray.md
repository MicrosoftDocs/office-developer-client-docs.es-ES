---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820681"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="42295-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="42295-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="42295-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42295-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42295-105">Crea una estructura de [SPropProblemArray](spropproblemarray.md) con nombre que contiene un número especificado de estructuras [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="42295-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42295-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="42295-106">Header file:</span></span>  <br/> |<span data-ttu-id="42295-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42295-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="42295-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="42295-108">Related structure:</span></span>  <br/> |<span data-ttu-id="42295-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="42295-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="42295-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42295-110">Parameters</span></span>

<span data-ttu-id="42295-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="42295-111">__cprob_</span></span>
  
> <span data-ttu-id="42295-112">Recuento de las estructuras de **SPropProblem** que se deben incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="42295-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="42295-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="42295-113">__name_</span></span>
  
> <span data-ttu-id="42295-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="42295-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42295-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42295-115">Remarks</span></span>

<span data-ttu-id="42295-116">Use la macro **SizedSPropProblemArray** para crear una matriz de propiedad problema con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="42295-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="42295-117">Para usar la nueva estructura que el resultado de la macro **SizedSPropProblemArray** como un puntero a una estructura **SPropProblemArray** , realice la conversión de tipos siguiente:</span><span class="sxs-lookup"><span data-stu-id="42295-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="42295-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="42295-118">See also</span></span>

- [<span data-ttu-id="42295-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="42295-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="42295-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="42295-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="42295-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="42295-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

