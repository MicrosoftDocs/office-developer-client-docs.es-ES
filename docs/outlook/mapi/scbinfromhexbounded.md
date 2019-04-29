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
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439761"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="93972-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="93972-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="93972-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93972-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93972-105">Convierte la parte especificada de una representación de cadena de un número hexadecimal en un número binario.</span><span class="sxs-lookup"><span data-stu-id="93972-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93972-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="93972-106">Header file:</span></span>  <br/> |<span data-ttu-id="93972-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="93972-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="93972-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="93972-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="93972-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="93972-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="93972-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="93972-110">Called by:</span></span>  <br/> |<span data-ttu-id="93972-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="93972-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="93972-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="93972-112">Parameters</span></span>

 <span data-ttu-id="93972-113">_SZ_</span><span class="sxs-lookup"><span data-stu-id="93972-113">_sz_</span></span>
  
> <span data-ttu-id="93972-114">a Puntero a la cadena terminada en null que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="93972-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="93972-115">Los caracteres válidos son los caracteres hexadecimales del 0 al 9 y los caracteres en mayúsculas y minúsculas de la a a la f.</span><span class="sxs-lookup"><span data-stu-id="93972-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="93972-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="93972-116">_pb_</span></span>
  
> <span data-ttu-id="93972-117">contempla Puntero al número binario devuelto.</span><span class="sxs-lookup"><span data-stu-id="93972-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="93972-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="93972-118">_cb_</span></span>
  
> <span data-ttu-id="93972-119">a Tamaño, en bytes, del parámetro _PB_ .</span><span class="sxs-lookup"><span data-stu-id="93972-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="93972-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93972-120">Return value</span></span>

<span data-ttu-id="93972-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="93972-121">S_OK</span></span>
  
> <span data-ttu-id="93972-122">La conversión se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="93972-122">Conversion was successful.</span></span>
    
<span data-ttu-id="93972-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="93972-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="93972-124">Se encontraron caracteres no válidos.</span><span class="sxs-lookup"><span data-stu-id="93972-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93972-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="93972-125">See also</span></span>



[<span data-ttu-id="93972-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="93972-126">FBinFromHex</span></span>](fbinfromhex.md)

