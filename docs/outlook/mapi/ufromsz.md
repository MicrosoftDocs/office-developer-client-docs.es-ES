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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439012"
---
# <a name="ufromsz"></a><span data-ttu-id="165fe-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="165fe-103">UFromSz</span></span>

  
  
<span data-ttu-id="165fe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="165fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="165fe-105">Convierte una cadena terminada en null de dígitos decimales en un entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="165fe-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="165fe-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="165fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="165fe-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="165fe-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="165fe-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="165fe-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="165fe-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="165fe-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="165fe-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="165fe-110">Called by:</span></span>  <br/> |<span data-ttu-id="165fe-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="165fe-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="165fe-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="165fe-112">Parameters</span></span>

 <span data-ttu-id="165fe-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="165fe-113">_lpsz_</span></span>
  
> <span data-ttu-id="165fe-114">[in] Puntero a la cadena terminada en null que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="165fe-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="165fe-115">El  _parámetro lpsz_ no debe superar los 65536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="165fe-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="165fe-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="165fe-116">Return value</span></span>

 <span data-ttu-id="165fe-117">**UFromSz** devuelve un entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="165fe-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="165fe-118">Si la cadena no comienza con al menos un dígito decimal, se devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="165fe-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="165fe-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="165fe-119">Remarks</span></span>

<span data-ttu-id="165fe-120">La **función UFromSz** deja de convertir cuando alcanza el primer carácter de la cadena que no es un dígito decimal.</span><span class="sxs-lookup"><span data-stu-id="165fe-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="165fe-121">Por ejemplo, teniendo en cuenta la cadena "55", **UFromSz** devuelve el valor entero 55.</span><span class="sxs-lookup"><span data-stu-id="165fe-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="165fe-122">Dada la cadena "5a5b", la función devuelve el valor entero 5.</span><span class="sxs-lookup"><span data-stu-id="165fe-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="165fe-123">Dada la cadena "a5b5", **UFromSz** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="165fe-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="165fe-124">**UFromSz es** sensible a las diferencias diacríticos.</span><span class="sxs-lookup"><span data-stu-id="165fe-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="165fe-125">Se admiten cadenas en los formatos Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="165fe-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="165fe-126">El límite de longitud de  _lpsz_ está en caracteres, no necesariamente bytes.</span><span class="sxs-lookup"><span data-stu-id="165fe-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

