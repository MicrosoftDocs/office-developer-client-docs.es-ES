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
ms.openlocfilehash: 363a85e1c6f111936b16e471eda6b9f962f8b65d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573624"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="ac284-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="ac284-103">SizedSPropTagArray</span></span>

<span data-ttu-id="ac284-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac284-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac284-105">Crea una estructura de [elemento SPropTagArray](sproptagarray.md) con nombre que incluye un número especificado de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ac284-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac284-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ac284-106">Header file:</span></span>  <br/> |<span data-ttu-id="ac284-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac284-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ac284-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="ac284-108">Related structure:</span></span>  <br/> |<span data-ttu-id="ac284-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="ac284-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="ac284-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac284-110">Parameters</span></span>

<span data-ttu-id="ac284-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="ac284-111">__ctag_</span></span>
  
> <span data-ttu-id="ac284-112">Recuento de etiquetas de propiedad que se deben incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="ac284-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="ac284-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="ac284-113">__name_</span></span>
  
> <span data-ttu-id="ac284-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="ac284-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac284-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac284-115">Remarks</span></span>

<span data-ttu-id="ac284-116">Use la macro **SizedSPropTagArray** para crear una matriz de etiqueta de propiedad con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="ac284-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="ac284-117">Para usar la nueva estructura que el resultado de la macro **SizedSPropTagArray** como un puntero a una estructura de **elemento SPropTagArray** , realice la conversión de tipos siguiente:</span><span class="sxs-lookup"><span data-stu-id="ac284-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="ac284-118">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ac284-118">See also</span></span>

- [<span data-ttu-id="ac284-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="ac284-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="ac284-120">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="ac284-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

