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
ms.openlocfilehash: bbced8412c2c3438c58af74ef072a46606b59ddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594617"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="5337d-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="5337d-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="5337d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5337d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5337d-105">Crea una estructura de [SPropProblemArray](spropproblemarray.md) con nombre que contiene un número especificado de estructuras [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="5337d-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5337d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5337d-106">Header file:</span></span>  <br/> |<span data-ttu-id="5337d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5337d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5337d-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="5337d-108">Related structure:</span></span>  <br/> |<span data-ttu-id="5337d-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="5337d-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="5337d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5337d-110">Parameters</span></span>

<span data-ttu-id="5337d-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="5337d-111">__cprob_</span></span>
  
> <span data-ttu-id="5337d-112">Recuento de las estructuras de **SPropProblem** que se deben incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="5337d-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="5337d-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="5337d-113">__name_</span></span>
  
> <span data-ttu-id="5337d-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="5337d-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5337d-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5337d-115">Remarks</span></span>

<span data-ttu-id="5337d-116">Use la macro **SizedSPropProblemArray** para crear una matriz de propiedad problema con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="5337d-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="5337d-117">Para usar la nueva estructura que el resultado de la macro **SizedSPropProblemArray** como un puntero a una estructura **SPropProblemArray** , realice la conversión de tipos siguiente:</span><span class="sxs-lookup"><span data-stu-id="5337d-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="5337d-118">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5337d-118">See also</span></span>

- [<span data-ttu-id="5337d-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="5337d-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="5337d-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="5337d-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="5337d-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="5337d-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

