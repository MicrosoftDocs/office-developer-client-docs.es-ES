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
ms.openlocfilehash: d5ba7e7bc52ba041e9fe6c9a01b35dc91d3b947b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820917"
---
# <a name="ulfromszhex"></a><span data-ttu-id="be9f2-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="be9f2-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="be9f2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be9f2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be9f2-105">Convierte una cadena terminada en null de dígitos hexadecimales en un entero largo sin signo.</span><span class="sxs-lookup"><span data-stu-id="be9f2-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be9f2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="be9f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="be9f2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be9f2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="be9f2-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="be9f2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="be9f2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="be9f2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="be9f2-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="be9f2-110">Called by:</span></span>  <br/> |<span data-ttu-id="be9f2-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="be9f2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="be9f2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be9f2-112">Parameters</span></span>

 <span data-ttu-id="be9f2-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="be9f2-113">_lpsz_</span></span>
  
> <span data-ttu-id="be9f2-114">[entrada] Puntero a la cadena terminada en null que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="be9f2-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="be9f2-115">El parámetro _lpsz_ no debe superar los caracteres, de 65536.</span><span class="sxs-lookup"><span data-stu-id="be9f2-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="be9f2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be9f2-116">Return value</span></span>

 <span data-ttu-id="be9f2-117">**UlFromSzHex** devuelve un entero largo sin signo.</span><span class="sxs-lookup"><span data-stu-id="be9f2-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="be9f2-118">Si la cadena no comienza con al menos un dígito hexadecimal, se devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="be9f2-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="be9f2-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="be9f2-119">Remarks</span></span>

<span data-ttu-id="be9f2-120">La función **UlFromSzHex** detiene la conversión cuando alcanza el primer carácter en la cadena que no es un dígito hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="be9f2-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="be9f2-121">Por ejemplo, dada la cadena "5a", **UlFromSzHex** devuelve el valor entero 90.</span><span class="sxs-lookup"><span data-stu-id="be9f2-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="be9f2-122">Dada la cadena "5g5h", la función devuelve el valor entero 5.</span><span class="sxs-lookup"><span data-stu-id="be9f2-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="be9f2-123">Dada la cadena "g5h5", **UlFromSzHex** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="be9f2-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="be9f2-124">**UlFromSzHex** es sensible a las diferencias diacríticas pero permite 'a' a 'f' y 'A' a 'F' de dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="be9f2-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="be9f2-125">Se admiten cadenas en los formatos de Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="be9f2-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="be9f2-126">El límite de longitud de _lpsz_ es en caracteres, no necesariamente bytes.</span><span class="sxs-lookup"><span data-stu-id="be9f2-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

