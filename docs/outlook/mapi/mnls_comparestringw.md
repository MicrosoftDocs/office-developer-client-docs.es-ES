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
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356850"
---
# <a name="mnls_comparestringw"></a><span data-ttu-id="8ddaf-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="8ddaf-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="8ddaf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ddaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ddaf-105">Compara dos cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="8ddaf-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="8ddaf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ddaf-106">Parameters</span></span>

 <span data-ttu-id="8ddaf-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="8ddaf-107">_lcid_</span></span>
  
> <span data-ttu-id="8ddaf-108">[entrada] Identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="8ddaf-108">[in] Locale identifier.</span></span> <span data-ttu-id="8ddaf-109">Para obtener definiciones detalladas, vea el parámetro  _Locale_ de [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ddaf-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="8ddaf-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="8ddaf-110">_dwFlags_</span></span>
  
> <span data-ttu-id="8ddaf-111">[entrada] Marcas para omitir mayúsculas y minúsculas y diacríticos.</span><span class="sxs-lookup"><span data-stu-id="8ddaf-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="8ddaf-112">Para obtener definiciones detalladas, vea el  _parámetro dwCmpFlags_ de [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ddaf-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="8ddaf-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="8ddaf-113">_pstr1_</span></span>
  
> <span data-ttu-id="8ddaf-114">[entrada] Puntero a la primera cadena Unicode que se compara.</span><span class="sxs-lookup"><span data-stu-id="8ddaf-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="8ddaf-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="8ddaf-115">_cch1_</span></span>
  
> <span data-ttu-id="8ddaf-116">[entrada] Longitud en caracteres de la primera cadena Unicode, excluyendo el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="8ddaf-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="8ddaf-117">La aplicación puede proporcionar un valor negativo si la cadena termina en null.</span><span class="sxs-lookup"><span data-stu-id="8ddaf-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="8ddaf-118">En este caso, **la MNLS_CompareStringW** función determina la longitud automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8ddaf-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="8ddaf-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="8ddaf-119">_pstr2_</span></span>
  
> <span data-ttu-id="8ddaf-120">[entrada] Puntero a la segunda cadena Unicode que se comparará.</span><span class="sxs-lookup"><span data-stu-id="8ddaf-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="8ddaf-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="8ddaf-121">_cch2_</span></span>
  
> <span data-ttu-id="8ddaf-122">[entrada] Longitud en caracteres de la segunda cadena Unicode, excluyendo el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="8ddaf-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="8ddaf-123">La aplicación puede proporcionar un valor negativo si la cadena termina en null.</span><span class="sxs-lookup"><span data-stu-id="8ddaf-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="8ddaf-124">En este caso, la función determina la longitud automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8ddaf-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8ddaf-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ddaf-125">Return value</span></span>

<span data-ttu-id="8ddaf-126">Devuelve los valores descritos para [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ddaf-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ddaf-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ddaf-127">Remarks</span></span>

<span data-ttu-id="8ddaf-128">Esta función ajusta [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ddaf-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="8ddaf-129">**MNLS_CompareStringW** toma los mismos parámetros y tiene el mismo comportamiento que [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ddaf-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ddaf-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8ddaf-130">See also</span></span>



[<span data-ttu-id="8ddaf-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="8ddaf-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="8ddaf-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="8ddaf-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

