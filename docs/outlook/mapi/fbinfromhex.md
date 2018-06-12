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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 64d205ee7f51c0ce6a6eb1e982659c6cda675f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816811"
---
# <a name="fbinfromhex"></a><span data-ttu-id="4c8fd-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="4c8fd-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="4c8fd-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c8fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4c8fd-105">Convierte una representación de cadena de un número hexadecimal en datos binarios.</span><span class="sxs-lookup"><span data-stu-id="4c8fd-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c8fd-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4c8fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="4c8fd-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4c8fd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4c8fd-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="4c8fd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4c8fd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4c8fd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4c8fd-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4c8fd-110">Called by:</span></span>  <br/> |<span data-ttu-id="4c8fd-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="4c8fd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="4c8fd-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c8fd-112">Parameters</span></span>

 <span data-ttu-id="4c8fd-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="4c8fd-113">_sz_</span></span>
  
> <span data-ttu-id="4c8fd-114">[entrada] Puntero a la cadena de ASCII terminada en null que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="4c8fd-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="4c8fd-115">No es una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="4c8fd-115">It is not a Unicode string.</span></span> <span data-ttu-id="4c8fd-116">Los caracteres válidos incluyen los caracteres hexadecimales cero a través de nueve y ambos caracteres en mayúsculas y minúsculas A la f el.</span><span class="sxs-lookup"><span data-stu-id="4c8fd-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="4c8fd-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="4c8fd-117">_pb_</span></span>
  
> <span data-ttu-id="4c8fd-118">[out] Puntero al número binario devuelto.</span><span class="sxs-lookup"><span data-stu-id="4c8fd-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c8fd-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c8fd-119">Return value</span></span>

<span data-ttu-id="4c8fd-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="4c8fd-120">TRUE</span></span> 
  
> <span data-ttu-id="4c8fd-121">La cadena se ha convertido correctamente en un número binario.</span><span class="sxs-lookup"><span data-stu-id="4c8fd-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="4c8fd-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="4c8fd-122">FALSE</span></span> 
  
> <span data-ttu-id="4c8fd-123">La cadena de entrada contiene caracteres no válidos de hexadecimal de ASCII.</span><span class="sxs-lookup"><span data-stu-id="4c8fd-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c8fd-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="4c8fd-124">See also</span></span>



[<span data-ttu-id="4c8fd-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="4c8fd-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

