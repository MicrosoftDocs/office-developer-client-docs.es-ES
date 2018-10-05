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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396214"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="98d36-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="98d36-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="98d36-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98d36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98d36-105">Compara dos cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="98d36-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="98d36-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98d36-106">Parameters</span></span>

 <span data-ttu-id="98d36-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="98d36-107">_lcid_</span></span>
  
> <span data-ttu-id="98d36-108">[entrada] Identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="98d36-108">[in] Locale identifier.</span></span> <span data-ttu-id="98d36-109">Para obtener definiciones detalladas, vea el parámetro de _Configuración regional_ de [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="98d36-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="98d36-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="98d36-110">_dwFlags_</span></span>
  
> <span data-ttu-id="98d36-111">[entrada] Marcas para pasar por alto mayúsculas y minúsculas y diacríticos.</span><span class="sxs-lookup"><span data-stu-id="98d36-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="98d36-112">Para obtener definiciones detalladas, vea el parámetro _dwCmpFlags_ de [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="98d36-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="98d36-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="98d36-113">_pstr1_</span></span>
  
> <span data-ttu-id="98d36-114">[entrada] Puntero a la primera cadena Unicode se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="98d36-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="98d36-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="98d36-115">_cch1_</span></span>
  
> <span data-ttu-id="98d36-116">[entrada] Longitud en caracteres de la primera cadena Unicode, excluyendo el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="98d36-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="98d36-117">La aplicación puede proporcionar un valor negativo si la cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="98d36-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="98d36-118">En este caso, la función **MNLS_CompareStringW** determina automáticamente la longitud.</span><span class="sxs-lookup"><span data-stu-id="98d36-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="98d36-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="98d36-119">_pstr2_</span></span>
  
> <span data-ttu-id="98d36-120">[entrada] Puntero a la segunda cadena Unicode se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="98d36-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="98d36-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="98d36-121">_cch2_</span></span>
  
> <span data-ttu-id="98d36-122">[entrada] Longitud en caracteres de la segunda cadena de Unicode, excluyendo el carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="98d36-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="98d36-123">La aplicación puede proporcionar un valor negativo si la cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="98d36-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="98d36-124">En este caso, la función determina automáticamente la longitud.</span><span class="sxs-lookup"><span data-stu-id="98d36-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98d36-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98d36-125">Return value</span></span>

<span data-ttu-id="98d36-126">Devuelve los valores que se describen para [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="98d36-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98d36-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98d36-127">Remarks</span></span>

<span data-ttu-id="98d36-128">Esta función ajusta [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="98d36-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="98d36-129">**MNLS_CompareStringW** acepta los mismos parámetros y tiene el mismo comportamiento como [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="98d36-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98d36-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="98d36-130">See also</span></span>



[<span data-ttu-id="98d36-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="98d36-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="98d36-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="98d36-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

