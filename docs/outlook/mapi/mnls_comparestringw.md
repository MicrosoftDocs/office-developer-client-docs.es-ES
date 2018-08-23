---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Última modificación: 20 de febrero de 2012'
ms.openlocfilehash: 3e23fa9fcb074fabacf1a2dd9ac3f632cdce5b5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576179"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="fc1bb-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="fc1bb-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="fc1bb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc1bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc1bb-105">Compara dos cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="fc1bb-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="fc1bb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc1bb-106">Parameters</span></span>

 <span data-ttu-id="fc1bb-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="fc1bb-107">_lcid_</span></span>
  
> <span data-ttu-id="fc1bb-108">[entrada] Identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="fc1bb-108">[in] Locale identifier.</span></span> <span data-ttu-id="fc1bb-109">Para obtener definiciones detalladas, vea el parámetro de _Configuración regional_ de [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fc1bb-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="fc1bb-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="fc1bb-110">_dwFlags_</span></span>
  
> <span data-ttu-id="fc1bb-111">[entrada] Marcas para pasar por alto mayúsculas y minúsculas y diacríticos.</span><span class="sxs-lookup"><span data-stu-id="fc1bb-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="fc1bb-112">Para obtener definiciones detalladas, vea el parámetro _dwCmpFlags_ de [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fc1bb-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="fc1bb-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="fc1bb-113">_pstr1_</span></span>
  
> <span data-ttu-id="fc1bb-114">[entrada] Puntero a la primera cadena Unicode se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="fc1bb-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="fc1bb-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="fc1bb-115">_cch1_</span></span>
  
> <span data-ttu-id="fc1bb-116">[entrada] Longitud en caracteres de la primera cadena Unicode, excluyendo el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="fc1bb-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="fc1bb-117">La aplicación puede proporcionar un valor negativo si la cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="fc1bb-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="fc1bb-118">En este caso, la función **MNLS_CompareStringW** determina automáticamente la longitud.</span><span class="sxs-lookup"><span data-stu-id="fc1bb-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="fc1bb-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="fc1bb-119">_pstr2_</span></span>
  
> <span data-ttu-id="fc1bb-120">[entrada] Puntero a la segunda cadena Unicode se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="fc1bb-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="fc1bb-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="fc1bb-121">_cch2_</span></span>
  
> <span data-ttu-id="fc1bb-122">[entrada] Longitud en caracteres de la segunda cadena de Unicode, excluyendo el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="fc1bb-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="fc1bb-123">La aplicación puede proporcionar un valor negativo si la cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="fc1bb-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="fc1bb-124">En este caso, la función determina automáticamente la longitud.</span><span class="sxs-lookup"><span data-stu-id="fc1bb-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc1bb-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc1bb-125">Return value</span></span>

<span data-ttu-id="fc1bb-126">Devuelve los valores que se describen para [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fc1bb-126">Returns the values described for [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fc1bb-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc1bb-127">Remarks</span></span>

<span data-ttu-id="fc1bb-128">Esta función ajusta [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fc1bb-128">This function wraps [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="fc1bb-129">**MNLS_CompareStringW** acepta los mismos parámetros y tiene el mismo comportamiento como [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fc1bb-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fc1bb-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fc1bb-130">See also</span></span>



[<span data-ttu-id="fc1bb-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="fc1bb-131">CompareStringW</span></span>](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="fc1bb-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="fc1bb-132">CompareStringEx</span></span>](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

