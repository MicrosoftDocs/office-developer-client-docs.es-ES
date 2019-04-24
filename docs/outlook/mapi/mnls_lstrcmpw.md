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
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356843"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="e84e0-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="e84e0-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="e84e0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e84e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e84e0-105">Compara dos cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="e84e0-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="e84e0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e84e0-106">Parameters</span></span>

 <span data-ttu-id="e84e0-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="e84e0-107">_lpString1_</span></span>
  
> <span data-ttu-id="e84e0-108">a Puntero a la primera cadena Unicode que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="e84e0-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="e84e0-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="e84e0-109">_lpString2_</span></span>
  
> <span data-ttu-id="e84e0-110">a Puntero a la segunda cadena Unicode que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="e84e0-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e84e0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e84e0-111">Return value</span></span>

<span data-ttu-id="e84e0-112">Devuelve los valores descritos para una llamada equivalente a **MNLS_CompareStringW** excepto para CSTR_EQUAL.</span><span class="sxs-lookup"><span data-stu-id="e84e0-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e84e0-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e84e0-113">Remarks</span></span>

 <span data-ttu-id="e84e0-114">_MNLS_lstrcmpW_ realiza una comparación llamando a [MNLS_CompareStringW](mnls_comparestringw.md) con una configuración regional de GetUserDefaultLCID, 0 para flags y-1 para cch1 y cch2.</span><span class="sxs-lookup"><span data-stu-id="e84e0-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e84e0-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="e84e0-115">See also</span></span>



[<span data-ttu-id="e84e0-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="e84e0-116">GetUserDefaultLCID</span></span>](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

