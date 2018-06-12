---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Última modificación: 18 de junio de 2012'
ms.openlocfilehash: 8ffd3c8337edcd96af6c3c4e425d274b21fee9f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818398"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="7a762-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="7a762-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="7a762-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a762-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a762-105">Compara dos cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="7a762-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="7a762-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a762-106">Parameters</span></span>

 <span data-ttu-id="7a762-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="7a762-107">_lpString1_</span></span>
  
> <span data-ttu-id="7a762-108">[entrada] Puntero a la primera cadena Unicode se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="7a762-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="7a762-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="7a762-109">_lpString2_</span></span>
  
> <span data-ttu-id="7a762-110">[entrada] Puntero a la segunda cadena Unicode se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="7a762-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a762-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a762-111">Return value</span></span>

<span data-ttu-id="7a762-112">Devuelve los valores que se describen para una llamada equivalente al **MNLS_CompareStringW** excepto CSTR_EQUAL.</span><span class="sxs-lookup"><span data-stu-id="7a762-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7a762-113">Notas</span><span class="sxs-lookup"><span data-stu-id="7a762-113">Remarks</span></span>

 <span data-ttu-id="7a762-114">_MNLS_lstrcmpW_ realiza una comparación mediante una llamada a [MNLS_CompareStringW](mnls_comparestringw.md) con una configuración regional de GetUserDefaultLCID, 0 para indicadores y -1 para cch1 y cch2.</span><span class="sxs-lookup"><span data-stu-id="7a762-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a762-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="7a762-115">See also</span></span>



[<span data-ttu-id="7a762-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="7a762-116">GetUserDefaultLCID</span></span>](http://msdn.microsoft.com/en-us/library/dd318135%28VS.85%29.aspx)

