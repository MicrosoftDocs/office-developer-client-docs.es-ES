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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386351"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="8be36-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="8be36-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="8be36-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8be36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8be36-105">Compara dos cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="8be36-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="8be36-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8be36-106">Parameters</span></span>

 <span data-ttu-id="8be36-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="8be36-107">_lpString1_</span></span>
  
> <span data-ttu-id="8be36-108">[entrada] Puntero a la primera cadena Unicode se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="8be36-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="8be36-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="8be36-109">_lpString2_</span></span>
  
> <span data-ttu-id="8be36-110">[entrada] Puntero a la segunda cadena Unicode se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="8be36-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8be36-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8be36-111">Return value</span></span>

<span data-ttu-id="8be36-112">Devuelve los valores que se describen para una llamada equivalente al **MNLS_CompareStringW** excepto CSTR_EQUAL.</span><span class="sxs-lookup"><span data-stu-id="8be36-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8be36-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8be36-113">Remarks</span></span>

 <span data-ttu-id="8be36-114">_MNLS_lstrcmpW_ realiza una comparación mediante una llamada a [MNLS_CompareStringW](mnls_comparestringw.md) con una configuración regional de GetUserDefaultLCID, 0 para indicadores y -1 para cch1 y cch2.</span><span class="sxs-lookup"><span data-stu-id="8be36-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8be36-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="8be36-115">See also</span></span>



[<span data-ttu-id="8be36-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="8be36-116">GetUserDefaultLCID</span></span>](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

