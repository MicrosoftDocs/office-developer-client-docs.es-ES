---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 5be5cd7c352201159c0257861c0072b56da65082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820927"
---
# <a name="ufromsz"></a><span data-ttu-id="e0f5d-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="e0f5d-103">UFromSz</span></span>

  
  
<span data-ttu-id="e0f5d-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0f5d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0f5d-105">Convierte una cadena terminada en null de dígitos decimales en un entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0f5d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e0f5d-106">Header file:</span></span>  <br/> |<span data-ttu-id="e0f5d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0f5d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e0f5d-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="e0f5d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e0f5d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e0f5d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e0f5d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e0f5d-110">Called by:</span></span>  <br/> |<span data-ttu-id="e0f5d-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="e0f5d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="e0f5d-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0f5d-112">Parameters</span></span>

 <span data-ttu-id="e0f5d-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="e0f5d-113">_lpsz_</span></span>
  
> <span data-ttu-id="e0f5d-114">[entrada] Puntero a la cadena terminada en null que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="e0f5d-115">El parámetro _lpsz_ no debe superar los caracteres, de 65536.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e0f5d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0f5d-116">Return value</span></span>

 <span data-ttu-id="e0f5d-117">**UFromSz** devuelve un entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="e0f5d-118">Si la cadena no comienza con al menos un dígito decimal, se devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e0f5d-119">Notas</span><span class="sxs-lookup"><span data-stu-id="e0f5d-119">Remarks</span></span>

<span data-ttu-id="e0f5d-120">La función **UFromSz** detiene la conversión cuando alcanza el primer carácter en la cadena que no es un dígito decimal.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="e0f5d-121">Por ejemplo, dada la cadena "55", **UFromSz** devuelve el valor entero 55.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="e0f5d-122">Dada la cadena "5a5b", la función devuelve el valor entero 5.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="e0f5d-123">Dada la cadena "a5b5", **UFromSz** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="e0f5d-124">**UFromSz** es sensible a las diferencias diacríticas.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="e0f5d-125">Se admiten cadenas en los formatos de Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="e0f5d-126">El límite de longitud de _lpsz_ es en caracteres, no necesariamente bytes.</span><span class="sxs-lookup"><span data-stu-id="e0f5d-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

