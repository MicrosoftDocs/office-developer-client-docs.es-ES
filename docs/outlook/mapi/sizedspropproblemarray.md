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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820681"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="c4d6e-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c4d6e-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="c4d6e-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4d6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4d6e-105">Crea una estructura de [SPropProblemArray](spropproblemarray.md) con nombre que contiene un número especificado de estructuras [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="c4d6e-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4d6e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c4d6e-106">Header file:</span></span>  <br/> |<span data-ttu-id="c4d6e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4d6e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c4d6e-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="c4d6e-108">Related structure:</span></span>  <br/> |<span data-ttu-id="c4d6e-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="c4d6e-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="c4d6e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4d6e-110">Parameters</span></span>

<span data-ttu-id="c4d6e-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="c4d6e-111">__cprob_</span></span>
  
> <span data-ttu-id="c4d6e-112">Recuento de las estructuras de **SPropProblem** que se deben incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="c4d6e-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="c4d6e-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="c4d6e-113">__name_</span></span>
  
> <span data-ttu-id="c4d6e-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="c4d6e-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4d6e-115">Notas</span><span class="sxs-lookup"><span data-stu-id="c4d6e-115">Remarks</span></span>

<span data-ttu-id="c4d6e-116">Use la macro **SizedSPropProblemArray** para crear una matriz de propiedad problema con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="c4d6e-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="c4d6e-117">Para usar la nueva estructura que el resultado de la macro **SizedSPropProblemArray** como un puntero a una estructura **SPropProblemArray** , realice la conversión de tipos siguiente:</span><span class="sxs-lookup"><span data-stu-id="c4d6e-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="c4d6e-118">Ver también</span><span class="sxs-lookup"><span data-stu-id="c4d6e-118">See also</span></span>

- [<span data-ttu-id="c4d6e-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c4d6e-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="c4d6e-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="c4d6e-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="c4d6e-121">Macros relacionadas con las estructuras</span><span class="sxs-lookup"><span data-stu-id="c4d6e-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

