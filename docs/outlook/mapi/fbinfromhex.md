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
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414938"
---
# <a name="fbinfromhex"></a><span data-ttu-id="08744-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="08744-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="08744-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08744-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08744-105">Convierte una representación de cadena de un número hexadecimal en datos binarios.</span><span class="sxs-lookup"><span data-stu-id="08744-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08744-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="08744-106">Header file:</span></span>  <br/> |<span data-ttu-id="08744-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="08744-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="08744-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="08744-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="08744-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="08744-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="08744-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="08744-110">Called by:</span></span>  <br/> |<span data-ttu-id="08744-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="08744-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="08744-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="08744-112">Parameters</span></span>

 <span data-ttu-id="08744-113">_SZ_</span><span class="sxs-lookup"><span data-stu-id="08744-113">_sz_</span></span>
  
> <span data-ttu-id="08744-114">a Puntero a la cadena ASCII terminada en null que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="08744-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="08744-115">No es una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="08744-115">It is not a Unicode string.</span></span> <span data-ttu-id="08744-116">Los caracteres válidos incluyen los caracteres hexadecimales del 0 al 9 y los caracteres en mayúsculas y minúsculas de la a a la F.</span><span class="sxs-lookup"><span data-stu-id="08744-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="08744-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="08744-117">_pb_</span></span>
  
> <span data-ttu-id="08744-118">contempla Puntero al número binario devuelto.</span><span class="sxs-lookup"><span data-stu-id="08744-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="08744-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08744-119">Return value</span></span>

<span data-ttu-id="08744-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="08744-120">TRUE</span></span> 
  
> <span data-ttu-id="08744-121">La cadena se convirtió correctamente en un número binario.</span><span class="sxs-lookup"><span data-stu-id="08744-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="08744-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="08744-122">FALSE</span></span> 
  
> <span data-ttu-id="08744-123">La cadena de entrada contiene caracteres hexadecimales ASCII no válidos.</span><span class="sxs-lookup"><span data-stu-id="08744-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08744-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="08744-124">See also</span></span>



[<span data-ttu-id="08744-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="08744-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

