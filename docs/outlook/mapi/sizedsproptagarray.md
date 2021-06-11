---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429351"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="998e3-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="998e3-103">SizedSPropTagArray</span></span>

<span data-ttu-id="998e3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="998e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="998e3-105">Crea una estructura [SPropTagArray con](sproptagarray.md) nombre que incluye un número especificado de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="998e3-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="998e3-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="998e3-106">Header file:</span></span>  <br/> |<span data-ttu-id="998e3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="998e3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="998e3-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="998e3-108">Related structure:</span></span>  <br/> |<span data-ttu-id="998e3-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="998e3-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="998e3-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="998e3-110">Parameters</span></span>

<span data-ttu-id="998e3-111">_ _ctag_</span><span class="sxs-lookup"><span data-stu-id="998e3-111">_ _ctag_</span></span>
  
> <span data-ttu-id="998e3-112">Recuento de etiquetas de propiedad que se incluirán en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="998e3-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="998e3-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="998e3-113">_ _name_</span></span>
  
> <span data-ttu-id="998e3-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="998e3-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="998e3-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="998e3-115">Remarks</span></span>

<span data-ttu-id="998e3-116">Use la **macro SizedSPropTagArray** para crear una matriz de etiquetas de propiedades con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="998e3-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="998e3-117">Para usar la nueva estructura que resulta de la macro **SizedSPropTagArray** como puntero a una estructura **SPropTagArray,** realice la conversión siguiente:</span><span class="sxs-lookup"><span data-stu-id="998e3-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="998e3-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="998e3-118">See also</span></span>

- [<span data-ttu-id="998e3-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="998e3-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="998e3-120">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="998e3-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

