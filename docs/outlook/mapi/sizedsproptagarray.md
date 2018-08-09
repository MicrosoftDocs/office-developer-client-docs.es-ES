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
ms.openlocfilehash: 7505c5dbcfc98a8b868424ae51cbe9c47b1d4338
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820684"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="6c803-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="6c803-103">SizedSPropTagArray</span></span>

<span data-ttu-id="6c803-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6c803-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6c803-105">Crea una estructura de [elemento SPropTagArray](sproptagarray.md) con nombre que incluye un número especificado de etiquetas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6c803-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c803-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="6c803-106">Header file:</span></span>  <br/> |<span data-ttu-id="6c803-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c803-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6c803-108">Estructura relacionado:</span><span class="sxs-lookup"><span data-stu-id="6c803-108">Related structure:</span></span>  <br/> |<span data-ttu-id="6c803-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="6c803-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="6c803-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c803-110">Parameters</span></span>

<span data-ttu-id="6c803-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="6c803-111">__ctag_</span></span>
  
> <span data-ttu-id="6c803-112">Recuento de etiquetas de propiedad que se deben incluir en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="6c803-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="6c803-113">__nombre_</span><span class="sxs-lookup"><span data-stu-id="6c803-113">__name_</span></span>
  
> <span data-ttu-id="6c803-114">Nombre de la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="6c803-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c803-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c803-115">Remarks</span></span>

<span data-ttu-id="6c803-116">Use la macro **SizedSPropTagArray** para crear una matriz de etiqueta de propiedad con límites explícitos.</span><span class="sxs-lookup"><span data-stu-id="6c803-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="6c803-117">Para usar la nueva estructura que el resultado de la macro **SizedSPropTagArray** como un puntero a una estructura de **elemento SPropTagArray** , realice la conversión de tipos siguiente:</span><span class="sxs-lookup"><span data-stu-id="6c803-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="6c803-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c803-118">See also</span></span>

- [<span data-ttu-id="6c803-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="6c803-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="6c803-120">Macros relacionadas con estructuras</span><span class="sxs-lookup"><span data-stu-id="6c803-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

