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
ms.openlocfilehash: f7889a255e2aa8ea4b6908f2f10a7b546a8ee3f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818396"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="7c911-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="7c911-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="7c911-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c911-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c911-105">Compara dos cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="7c911-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="7c911-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c911-106">Parameters</span></span>

 <span data-ttu-id="7c911-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="7c911-107">_lcid_</span></span>
  
> <span data-ttu-id="7c911-108">[entrada] Identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="7c911-108">[in] Locale identifier.</span></span> <span data-ttu-id="7c911-109">Para obtener definiciones detalladas, vea el parámetro de _Configuración regional_ de [CompareString](http://msdn.microsoft.com/es-es/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7c911-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](http://msdn.microsoft.com/es-es/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="7c911-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="7c911-110">_dwFlags_</span></span>
  
> <span data-ttu-id="7c911-111">[entrada] Marcas para pasar por alto mayúsculas y minúsculas y diacríticos.</span><span class="sxs-lookup"><span data-stu-id="7c911-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="7c911-112">Para obtener definiciones detalladas, vea el parámetro _dwCmpFlags_ de [CompareStringEx](http://msdn.microsoft.com/es-es/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7c911-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](http://msdn.microsoft.com/es-es/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="7c911-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="7c911-113">_pstr1_</span></span>
  
> <span data-ttu-id="7c911-114">[entrada] Puntero a la primera cadena Unicode se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="7c911-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="7c911-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="7c911-115">_cch1_</span></span>
  
> <span data-ttu-id="7c911-116">[entrada] Longitud en caracteres de la primera cadena Unicode, excluyendo el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="7c911-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="7c911-117">La aplicación puede proporcionar un valor negativo si la cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="7c911-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="7c911-118">En este caso, la función **MNLS_CompareStringW** determina automáticamente la longitud.</span><span class="sxs-lookup"><span data-stu-id="7c911-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="7c911-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="7c911-119">_pstr2_</span></span>
  
> <span data-ttu-id="7c911-120">[entrada] Puntero a la segunda cadena Unicode se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="7c911-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="7c911-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="7c911-121">_cch2_</span></span>
  
> <span data-ttu-id="7c911-122">[entrada] Longitud en caracteres de la segunda cadena de Unicode, excluyendo el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="7c911-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="7c911-123">La aplicación puede proporcionar un valor negativo si la cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="7c911-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="7c911-124">En este caso, la función determina automáticamente la longitud.</span><span class="sxs-lookup"><span data-stu-id="7c911-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c911-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c911-125">Return value</span></span>

<span data-ttu-id="7c911-126">Devuelve los valores que se describen para [CompareStringEx](http://msdn.microsoft.com/es-es/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7c911-126">Returns the values described for [CompareStringEx](http://msdn.microsoft.com/es-es/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c911-127">Notas</span><span class="sxs-lookup"><span data-stu-id="7c911-127">Remarks</span></span>

<span data-ttu-id="7c911-128">Esta función ajusta [CompareStringW](http://msdn.microsoft.com/es-es/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7c911-128">This function wraps [CompareStringW](http://msdn.microsoft.com/es-es/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="7c911-129">**MNLS_CompareStringW** acepta los mismos parámetros y tiene el mismo comportamiento como [CompareStringW](http://msdn.microsoft.com/es-es/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7c911-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](http://msdn.microsoft.com/es-es/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7c911-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="7c911-130">See also</span></span>



[<span data-ttu-id="7c911-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="7c911-131">CompareStringW</span></span>](http://msdn.microsoft.com/es-es/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="7c911-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="7c911-132">CompareStringEx</span></span>](http://msdn.microsoft.com/es-es/library/dd317761%28VS.85%29.aspx)

