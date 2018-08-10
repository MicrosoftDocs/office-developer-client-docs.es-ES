---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a00a9b2200f76dfd600f72bf387467b5792599c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820561"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="35968-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="35968-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="35968-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35968-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35968-105">Convierte la parte especificada de una representación de cadena de un número hexadecimal en un número binario.</span><span class="sxs-lookup"><span data-stu-id="35968-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35968-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="35968-106">Header file:</span></span>  <br/> |<span data-ttu-id="35968-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="35968-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="35968-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="35968-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="35968-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="35968-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="35968-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="35968-110">Called by:</span></span>  <br/> |<span data-ttu-id="35968-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="35968-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="35968-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35968-112">Parameters</span></span>

 <span data-ttu-id="35968-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="35968-113">_sz_</span></span>
  
> <span data-ttu-id="35968-114">[entrada] Puntero a la cadena terminada en null que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="35968-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="35968-115">Los caracteres válidos incluyen los caracteres hexadecimales 0 a 9 y los caracteres en mayúsculas y minúsculas a la f.</span><span class="sxs-lookup"><span data-stu-id="35968-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="35968-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="35968-116">_pb_</span></span>
  
> <span data-ttu-id="35968-117">[out] Puntero al número binario devuelto.</span><span class="sxs-lookup"><span data-stu-id="35968-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="35968-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="35968-118">_cb_</span></span>
  
> <span data-ttu-id="35968-119">[entrada] Tamaño, en bytes, del parámetro _pb_ .</span><span class="sxs-lookup"><span data-stu-id="35968-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="35968-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35968-120">Return value</span></span>

<span data-ttu-id="35968-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="35968-121">S_OK</span></span>
  
> <span data-ttu-id="35968-122">Conversión fue correcta.</span><span class="sxs-lookup"><span data-stu-id="35968-122">Conversion was successful.</span></span>
    
<span data-ttu-id="35968-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="35968-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="35968-124">Se encontraron caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="35968-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="35968-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="35968-125">See also</span></span>



[<span data-ttu-id="35968-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="35968-126">FBinFromHex</span></span>](fbinfromhex.md)

