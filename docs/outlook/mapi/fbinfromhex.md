---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 87a470c1c682225eb1deefba9ccc8c12fbdc49c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569830"
---
# <a name="fbinfromhex"></a><span data-ttu-id="9babb-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="9babb-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="9babb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9babb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9babb-105">Convierte una representación de cadena de un número hexadecimal en datos binarios.</span><span class="sxs-lookup"><span data-stu-id="9babb-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9babb-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9babb-106">Header file:</span></span>  <br/> |<span data-ttu-id="9babb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9babb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9babb-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="9babb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9babb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9babb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9babb-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9babb-110">Called by:</span></span>  <br/> |<span data-ttu-id="9babb-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="9babb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="9babb-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9babb-112">Parameters</span></span>

 <span data-ttu-id="9babb-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="9babb-113">_sz_</span></span>
  
> <span data-ttu-id="9babb-114">[entrada] Puntero a la cadena de ASCII terminada en null que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="9babb-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="9babb-115">No es una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="9babb-115">It is not a Unicode string.</span></span> <span data-ttu-id="9babb-116">Los caracteres válidos incluyen los caracteres hexadecimales cero a través de nueve y ambos caracteres en mayúsculas y minúsculas A la f el.</span><span class="sxs-lookup"><span data-stu-id="9babb-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="9babb-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="9babb-117">_pb_</span></span>
  
> <span data-ttu-id="9babb-118">[out] Puntero al número binario devuelto.</span><span class="sxs-lookup"><span data-stu-id="9babb-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9babb-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9babb-119">Return value</span></span>

<span data-ttu-id="9babb-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="9babb-120">TRUE</span></span> 
  
> <span data-ttu-id="9babb-121">La cadena se ha convertido correctamente en un número binario.</span><span class="sxs-lookup"><span data-stu-id="9babb-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="9babb-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="9babb-122">FALSE</span></span> 
  
> <span data-ttu-id="9babb-123">La cadena de entrada contiene caracteres no válidos de hexadecimal de ASCII.</span><span class="sxs-lookup"><span data-stu-id="9babb-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9babb-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9babb-124">See also</span></span>



[<span data-ttu-id="9babb-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="9babb-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

