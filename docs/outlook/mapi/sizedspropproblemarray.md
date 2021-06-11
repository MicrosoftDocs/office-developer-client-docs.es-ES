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
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418116"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="4f721-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="4f721-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="4f721-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f721-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f721-105">Crea una estructura [SPropProblemArray](spropproblemarray.md) con nombre que contiene un número especificado de estructuras [SPropProblem.](spropproblem.md)</span><span class="sxs-lookup"><span data-stu-id="4f721-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f721-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4f721-106">Header file:</span></span>  <br/> |<span data-ttu-id="4f721-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f721-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4f721-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="4f721-108">Related structure:</span></span>  <br/> |<span data-ttu-id="4f721-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="4f721-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="4f721-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="4f721-110">Parameters</span></span>

<span data-ttu-id="4f721-111">_ _cprob_</span><span class="sxs-lookup"><span data-stu-id="4f721-111">_ _cprob_</span></span>
  
> <span data-ttu-id="4f721-112">Recuento de **estructuras SPropProblem** que se incluirán en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="4f721-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="4f721-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="4f721-113">_ _name_</span></span>
  
> <span data-ttu-id="4f721-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="4f721-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f721-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f721-115">Remarks</span></span>

<span data-ttu-id="4f721-116">Use la **macro SizedSPropProblemArray** para crear una matriz de problemas de propiedad con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="4f721-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="4f721-117">Para usar la nueva estructura que resulta de la macro **SizedSPropProblemArray** como puntero a una estructura **SPropProblemArray,** realice la conversión siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f721-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="4f721-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f721-118">See also</span></span>

- [<span data-ttu-id="4f721-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="4f721-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="4f721-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="4f721-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="4f721-121">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="4f721-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

