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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282701"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="988d1-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="988d1-103">SizedSPropTagArray</span></span>

<span data-ttu-id="988d1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="988d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="988d1-105">Crea una estructura [SPropTagArray](sproptagarray.md) con nombre que incluye un número especificado de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="988d1-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="988d1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="988d1-106">Header file:</span></span>  <br/> |<span data-ttu-id="988d1-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="988d1-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="988d1-108">Estructura relacionada:</span><span class="sxs-lookup"><span data-stu-id="988d1-108">Related structure:</span></span>  <br/> |<span data-ttu-id="988d1-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="988d1-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="988d1-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="988d1-110">Parameters</span></span>

<span data-ttu-id="988d1-111">__CTAG_</span><span class="sxs-lookup"><span data-stu-id="988d1-111">__ctag_</span></span>
  
> <span data-ttu-id="988d1-112">Número de etiquetas de propiedad que se van a incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="988d1-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="988d1-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="988d1-113">__name_</span></span>
  
> <span data-ttu-id="988d1-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="988d1-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="988d1-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="988d1-115">Remarks</span></span>

<span data-ttu-id="988d1-116">Use la macro **SizedSPropTagArray** para crear una matriz de etiquetas de propiedad con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="988d1-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="988d1-117">Para usar la nueva estructura que resulta de la macro **SizedSPropTagArray** como un puntero a una estructura **SPropTagArray** , realice la siguiente conversión:</span><span class="sxs-lookup"><span data-stu-id="988d1-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="988d1-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="988d1-118">See also</span></span>

- [<span data-ttu-id="988d1-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="988d1-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="988d1-120">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="988d1-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

