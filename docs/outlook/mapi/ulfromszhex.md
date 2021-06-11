---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433055"
---
# <a name="ulfromszhex"></a><span data-ttu-id="e1666-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="e1666-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="e1666-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1666-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1666-105">Convierte una cadena terminada en null de dígitos hexadecimales en un entero largo sin signo.</span><span class="sxs-lookup"><span data-stu-id="e1666-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1666-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e1666-106">Header file:</span></span>  <br/> |<span data-ttu-id="e1666-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1666-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e1666-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e1666-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e1666-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e1666-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e1666-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e1666-110">Called by:</span></span>  <br/> |<span data-ttu-id="e1666-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="e1666-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="e1666-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e1666-112">Parameters</span></span>

 <span data-ttu-id="e1666-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="e1666-113">_lpsz_</span></span>
  
> <span data-ttu-id="e1666-114">[in] Puntero a la cadena terminada en null que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="e1666-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="e1666-115">El  _parámetro lpsz_ no debe superar los 65536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e1666-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e1666-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1666-116">Return value</span></span>

 <span data-ttu-id="e1666-117">**UlFromSzHex** devuelve un entero largo sin signo.</span><span class="sxs-lookup"><span data-stu-id="e1666-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="e1666-118">Si la cadena no comienza con al menos un dígito hexadecimal, se devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e1666-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e1666-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1666-119">Remarks</span></span>

<span data-ttu-id="e1666-120">La **función UlFromSzHex** deja de convertir cuando alcanza el primer carácter de la cadena que no es un dígito hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="e1666-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="e1666-121">Por ejemplo, teniendo en cuenta la cadena "5a", **UlFromSzHex** devuelve el valor entero 90.</span><span class="sxs-lookup"><span data-stu-id="e1666-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="e1666-122">Dada la cadena "5g5h", la función devuelve el valor entero 5.</span><span class="sxs-lookup"><span data-stu-id="e1666-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="e1666-123">Dada la cadena "g5h5", **UlFromSzHex** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e1666-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="e1666-124">**UlFromSzHex** es sensible a las diferencias diacríticos, pero permite tanto 'a' a 'f' como 'A' a 'F' para dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="e1666-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="e1666-125">Se admiten cadenas en los formatos Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="e1666-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="e1666-126">El límite de longitud de  _lpsz_ está en caracteres, no necesariamente bytes.</span><span class="sxs-lookup"><span data-stu-id="e1666-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

